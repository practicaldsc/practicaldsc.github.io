---
layout: page
title: Regularization
description: >-
  More details on regularization in the context of linear regression.
parent: 🤖 Machine Learning
grand_parent: 🧑‍🤝‍🧑 Guides
---

# {{ page.title }}
{:.no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

{: .blue }

> This guide is designed to:
> 1. Give you a better understanding of regularization, as covered in [Lecture 19](https://practicaldsc.org/resources/lectures/lec19/lec19-filled.html).
> 2. Prepare you for Homework 9, Question 1, which is on the theory of regularization.
>
> This guide is essential, but it is **not** a substitute for reading and watching Lecture 19.

---

<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"> </script>

## Overview

As we will see in Lecture 19, **ridge regression** is the problem of finding the vector $$\vec{w}$$ that minimizes the following **objective function**:

$$R_\text{ridge}(\vec{w}) = \frac{1}{n} \lVert \vec{y} - X \vec{w} \rVert_2^2 + \underbrace{\lambda \sum_{j = 1}^d w_j^2}_{\text{penalty!}}$$

Once we find that vector, we can make predictions using $$\vec{h} = X \vec{w}_\text{ridge}^*$$, where $$X$$ is a design matrix with information about the individuals we want to make predictions for. The fact that we've added a penalty, $$\lambda \sum_{j = 1}^d w_j^2$$, to our objective function means that we are regularizing our objective function, i.e. we are performing **regularization**. 

The vector that minimizes $$R_\text{ridge}(\vec{w})$$ is:

$$\vec{w}_\text{ridge}^* = (X^TX + n \lambda I)^{-1} X^T \vec{y}$$

$$\vec{w}_\text{ridge}^*$$ is unique, whether or not $$X$$ is full rank. 

This is different from $$\vec{w}_\text{OLS}^* = (X^TX)^{-1}X^T \vec{y}$$, which is only uniquely defined when $$X^TX$$ is invertible; otherwise, all of the infinitely many solutions to the normal equations, $$X^TX \vec{w}_\text{OLS}^* = X^T \vec{y}$$, minimize mean squared error. Remember, "OLS" refers to "ordinary least squares", the process of minimizing mean squared error, $$R_\text{sq}(\vec{w}) = \frac{1}{n} \lVert \vec y - X \vec w \rVert_2^2$$, with no regularization.

Some lingering questions:
- When there are infinitely many solutions to the normal equations, which solution(s) does Python return?
- Why is it called ridge regression?
- Why is $$\vec{w}_\text{ridge}^*$$ always uniquely-defined, i.e. why does the ridge regression objective function always have a unique solution?

The purpose of this guide is to explore these lingering ideas.

---

## Framing the Problem

To start, we load in the dataset containing the weights and heights of 25,000 18 year olds we used in Lecture 16 to demonstrate multicollinearity.

```python
heights.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Height (Inches)</th>
      <th>Height (Feet)</th>
      <th>Weight (Pounds)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>65.78331</td>
      <td>5.481942</td>
      <td>112.9925</td>
    </tr>
    <tr>
      <th>1</th>
      <td>71.51521</td>
      <td>5.959601</td>
      <td>136.4873</td>
    </tr>
    <tr>
      <th>2</th>
      <td>69.39874</td>
      <td>5.783228</td>
      <td>153.0269</td>
    </tr>
    <tr>
      <th>3</th>
      <td>68.21660</td>
      <td>5.684717</td>
      <td>142.3354</td>
    </tr>
    <tr>
      <th>4</th>
      <td>67.78781</td>
      <td>5.648984</td>
      <td>144.2971</td>
    </tr>
  </tbody>
</table>
</div>

Note that there are two height columns, `'Height (Inches)'` and `'Height (Feet)'`. Remember that 1 foot is equal to 12 inches, so the values in the `'Height (Inches)'` column are 12 times the values in the `'Height (Feet)'` column.

Throughout this question, we'll aim to predict `'Weight (Pounds)'` using the other two features. Let's start by plotting `'Weight (Pounds)'` vs. `'Height (Inches)'`:

<center>
<iframe src="../assets/ridge-1.html" width="85%" height="400" frameborder="0"></iframe>
</center>

And `'Weight (Pounds)'` vs. `'Height (Inches)'` and `'Height (Feet)'`:

<iframe src="../assets/ridge-2.html" width="85%" height="400" frameborder="0"></iframe>

Drag the plot above around. You should notice that the points form a flat "patty" that resembles the 2D plot from above, not a cloud ☁️
like in other 3D scatter plots we've seen in class. This is because `'Height (Feet)'` and `'Height (Inches)'` are the same values, just in different units. For a particular `'Height (Feet)'` value, there is only one possible `'Height (Inches)'` value – specifically, 12 times the `'Height (Feet)'` value – and so all points in the plot sit on the flat plane:

$$\text{Height (Inches)} = 12 \cdot \text{Height (Feet)}$$

We'll start by fitting a multiple linear regression model to predict `'Weight (Pounds)'` from `'Height (Inches)'` and `'Height (Feet)'`, without regularization. Our model is of the form:

$$\text{predicted Weight (Pounds)}_i = w_0 + w_1 \cdot \text{Height (Inches)}_i + w_2 \cdot \text{Height (Feet)}_i$$

```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(people[['Height (Inches)', 'Height (Feet)']], 
                                                    people['Weight (Pounds)'])
```

The design matrix for our training data, `X_train_design`, is defined below:

```python
X_train_design = X_train.copy()
X_train_design['1'] = 1
X_train_design = X_train_design[['1', 'Height (Inches)', 'Height (Feet)']]
X_train_design
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>1</th>
      <th>Height (Inches)</th>
      <th>Height (Feet)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>10903</th>
      <td>1</td>
      <td>68.92271</td>
      <td>5.743559</td>
    </tr>
    <tr>
      <th>7740</th>
      <td>1</td>
      <td>65.18871</td>
      <td>5.432392</td>
    </tr>
    <tr>
      <th>6636</th>
      <td>1</td>
      <td>70.49243</td>
      <td>5.874369</td>
    </tr>
    <tr>
      <th>23722</th>
      <td>1</td>
      <td>68.71113</td>
      <td>5.725928</td>
    </tr>
    <tr>
      <th>10148</th>
      <td>1</td>
      <td>65.69257</td>
      <td>5.474381</td>
    </tr>
  </tbody>
</table>

We know that our design matrix isn't full rank. Python knows this, too:

```python
np.linalg.matrix_rank(X_train_design)
```

```
2
```

Note that $$X$$ and $$X^TX$$ have the same rank:

```python
np.linalg.matrix_rank(X_train_design.T @ X_train_design)
```

```
2
```

So, $$X^TX$$ is not invertible, and there are infinitely many solutions to the normal equations, 

$$X^TX \vec{w}_\text{OLS}^* = X^T \vec{y}$$

No line of code can return an infinitely long output (at least, not in finite time), so there's no way to see **all** of the infinitely many possible solutions in code. Instead, to find the relationship between the infinitely many possible $$\vec{w}^*_\text{OLS}$$ values, we'd need to think about the relationship between our multicollinear features, like we did in [Lecture 17](https://practicaldsc.org/resources/lectures/lec17/lec17-filled.html#Redundant-features).

---

## Solving the Normal Equations under Multicollinearity

It turns out that there are several different ways we can _try_ and solve the normal equations in Python – and many of them give different results! Let's enumerate some possibilities.


### `np.linalg.inv`

First, we can try and use `np.linalg.inv` and try and evaluate $$\vec{w}_\text{OLS}^* = (X^TX)^{-1} X^T \vec{y}$$ directly. It's not clear why this should work, since $$X^TX$$ is **not** invertible. Nevertheless, Python gives us _some_ result!

```python
w_inv = np.linalg.inv(X_train_design.T @ X_train_design) @ X_train_design.T @ y_train
w_inv = w_inv.to_numpy()
w_inv
```

```
array([-59.93693329,   2.43212549,  10.06693352])
```

### `np.linalg.pinv`

We can use the same approach as above, but instead use `np.linalg.pinv`, which computes the **pseudoinverse** of its argument. The pseudoinverse is the generalization of the matrix inverse to non-invertible matrices; read more [here](https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse).

```python
w_pinv = np.linalg.pinv(X_train_design.T @ X_train_design) @ X_train_design.T @ y_train
w_pinv = w_pinv.to_numpy()
w_pinv
```

```
array([-82.77005461,   3.06489359,   0.25540779])
```

### `np.linalg.solve`

We can use `np.linalg.solve` to "solve" the normal equations, $$X^TX \vec{w}_\text{OLS}^* = X^T \vec{y}$$, without needing to invert. Remember, the normal equations are a system of $$d+1$$ equations with $$d+1$$ unknowns ($$w_0^*, w_1^*, ..., w_d^*$$); here, we have $$d = 2$$ features.

```python
w_solve = np.linalg.solve(X_train_design.T @ X_train_design, X_train_design.T @ y_train)
w_solve
```

```
array([-82.77005461,   7.47197413, -52.62955865])
```

### `np.linalg.lstsq`

We can also use `np.linalg.lstsq`. `np.linalg.lstsq(A, B)` returns the vector $$\vec{w}$$ that minimizes $$\frac{1}{n} \lVert B - A \vec{w} \rVert_2^2$$. For us, `A = X_train_design` and `B = y_train`.

```python
w_lstsq = np.linalg.lstsq(X_train_design, y_train)[0]
w_lstsq
```

```python
array([-8.27700546e+01, -3.59298640e+11,  4.31158369e+12])
```

### `sklearn`

Finally, we can just use `sklearn`, as we've done in class and homeworks already.

```python
from sklearn.linear_model import LinearRegression

# Our design matrix already has a column of 1s, so we don't need to tell sklearn to fit an intercept.
model = LinearRegression(fit_intercept=False) 
model.fit(X_train_design, y_train)

w_sklearn = model.coef_
w_sklearn
```

```python
array([-82.77005461,   3.06489359,   0.2554078 ])
```

Hmm... all five methods were in theory solving the same problem, and so should have given us the same optimal parameter vector, $$\vec{w}_\text{OLS}^*$$, but the first four were slightly different. The last two were identical; upon further investigation, [`sklearn`'s documentation](https://scikit-learn.org/1.5/modules/generated/sklearn.linear_model.LinearRegression.html) shows us that LinearRegression's `fit` method just calls `np.linalg.lstsq` under the hood!

While many of the $$\vec{w}_\text{OLS}^*$$ vectors look different, many (but not all!) end up making the same predictions and have the same mean squared error. Let's take a look:

TODO

It seems that the last four $$\vec{w}_\text{OLS}^*$$ vectors made the same predictions and had the same minimal mean squared error of $$\approx 101.31$$, while the optimal $$\vec{w}_\text{OLS}^*$$ found using `np.linalg.inv` **wasn't** actually optimal, since it didn't have the minimal mean squared error! (There were minor differences between the last four, but these differences are attributed to the fact that the techniques use different numerical methods to solve for the necessary vectors with different stopping criteria, and due to the general imprecision of floating-point arithmetic.)

This tells us that `np.linalg.inv` does _something_ when the input matrix is not invertible, and the result isn't reliable, at least not in the context of solving the normal equations.

But generally, it seems that when the design matrix isn't full rank, we still can minimize mean squared error, it's just unclear which "optimal" parameter vector $$\vec{w}_\text{OLS}^*$$ we'll end up with, since there are infinitely many choices that minimize MSE. This is an issue if we care about interpreting the coefficients of our model.

---

## Ridge to the Rescue

**So, how does ridge regression help with this problem?**

To illustrate, let's look at a graph of $$R_\text{ridge}(\vec{w}) = \frac{1}{n} \lVert \vec y - X \vec w \rVert_2^2 + \lambda \sum_{j = 1}^d w_j^2$$, for different values of $$\lambda$$. The graph you're about to see is also known as a _loss surface_.

Remember, our model is of the form:

$$\text{predicted Weight (Pounds)}_i = w_0 + w_1 \cdot \text{Height (Inches)}_i + w_2 \cdot \text{Height (Feet)}_i$$

There are three axes in the graph that appears:

- One for different values of $$w_1$$.
- One for different values of $$w_2$$.
- One for the value of $$R_\text{ridge}(-82.77, w_1, w_2)$$$. Since we have three parameters, we'd need four axes to truly visualize $$R_\text{ridge}(\vec{w})$$, so we've fixed a particular value of $$w_0$$. (The interesting part of the graph doesn't involve the intercept, anyways, since the multicollinearity is between `'Height (Inches)'` and `'Height (Feet)'`.)

Run the cell below and interact with the slider that appears!

TODO

Some things to note:
- When you drag the `reg_lambda` slider to 0, and see the title "Mean Squared Error", you should notice a long "ridge" at the bottom of the loss surface! All values of $$w_1$$ and $$w_2$$ that fall on that ridge minimize mean squared error. **This ridge is problematic!**
- As you increase `reg_lambda`, the surface looks more and more like a bowl curved upwards, and less "ridgy". **Ridge regression removes the ridge!**
- As you increase `reg_lambda`, look at the $$z$$-axis of the resulting plot.

So, there, we have our answer! Ridge regression removes the "ridge" of infinitely many solutions when multicollinearity is present.

What we _haven't_ really answered is **why?** Why does the ridge regression objective function always have a unique minimizer, $$\vec{w}_\text{ridge}^*$$? That's what we'll work through now.

---

## Properties of Ridge Regression

Throughout the remainder of this guide, we'll call the regularization penalty $$\lambda_\text{ridge}$$, not just $$\lambda$$, to avoid confusion with other notation we're about to introduce.

We've just taken for granted the fact that the minimizer of the ridge regression objective function,

$$R_\text{ridge}(\vec{w}) = \frac{1}{n} \lVert \vec{y} - X \vec{w} \rVert_2^2 + \lambda_\text{ridge} \sum_{j = 1}^d w_j^2$$

is:

$$\vec{w}_\text{ridge}^* = (X^TX + n \lambda_\text{ridge} I)^{-1} X^T \vec{y}$$

In Homework 9, we'll have you prove that this indeed is the minimizer. But for now, we'll answer the question, **why is $$\vec{w}_\text{ridge}^*$$ always uniquely defined?** This problem boils down to determining why $$X^TX + n \lambda_\text{ridge} I$$ is always invertible, since the inverse of a matrix – **if it exists** – is always unique.

To prove that $$X^TX + n \lambda_\text{ridge} I$$ is always invertible, we'll need to remember how eigenvalues and eigenvectors work from linear algebra. If you don't remember (or never learned), don't worry – we'll explain everything that's relevant. (And yes, this is all relevant to understanding how ridge regression works!)

$$\lambda_i$$ is an **eigenvalue** of square matrix $$A$$, corresponding to the **eigenvector** $$\vec{v}_i$$, if:

$$A \vec{v}_i = \lambda_i \vec{v}_i$$

In other words, $\vec{v}_i$ is an eigenvalue of $A$ if, when left-multiplied by $A$, its direction doesn't change, only its length. The amount $\vec{v}_i$'s length is scaled by is $\lambda_i$. We also say that $\lambda_i$ and $\vec{v}_i$ form an **eigenvalue-eigenvector pair of $A$**. (Note that $\vec{0}$ is never considered to be an eigenvector, since any matrix times $\vec{0}$ is always just $\vec{0}$.)

For example, if $A = \begin{bmatrix} -5 & 2 \\ -7 & 4 \end{bmatrix}$, then $\vec{v}_1 = \begin{bmatrix} 2 \\ 7 \end{bmatrix}$ is an eigenvector of $A$ corresponding to the eigenvalue $\lambda_1 = 2$, because:

$$A\vec{v}_1 = \begin{bmatrix} -5 & 2 \\ -7 & 4 \end{bmatrix} \begin{bmatrix} 2 \\ 7 \end{bmatrix} = \begin{bmatrix} -5(2) + 2(7) \\ -7(2) + 4(7) \end{bmatrix} = \begin{bmatrix} 4 \\ 14 \end{bmatrix} = 2 \begin{bmatrix} 2 \\ 7 \end{bmatrix} = 2 \vec{v}_1$$

So, when $\vec{v}_1$ is multiplied by $A$, it still points in the same direction, it's just doubled in length.

**Verify yourself that $\lambda_2 = -3$ is also an eigenvalue of $A$, corresponding to the eigenvector $\vec{v}_2 = \begin{bmatrix} 1 \\ 1\end{bmatrix}$.** Read more about eigenvalues and eigenvectors [**here**](https://math.libretexts.org/Bookshelves/Linear_Algebra/A_First_Course_in_Linear_Algebra_(Kuttler)/07%3A_Spectral_Theory/7.01%3A_Eigenvalues_and_Eigenvectors_of_a_Matrix), though we will cover everything you need to know directly in this homework.

One more thing: an $n \times n$ matrix can have at most $n$ non-zero eigenvalues. The **rank** of a square matrix is equal to the number of non-zero eigenvalues it has.

<br>

Okay, so what did we need all of that for? It's to use this fact:

<center><b>A square matrix is invertible <i>if and only if</i> none of its eigenvalues are 0.</b></center>

We will use this particular fact without proof, mostly because its proof is similar to the proof you're about to do yourself. If we can prove that none of $X^TX + n \lambda_\text{ridge} I$'s eigenvalues are 0, then we know it must be invertible, and so $\vec{w}_\text{ridge}^*$ is uniquely defined. This is especially useful if some of $X^TX$'s eigenvalues are 0, which is the case when $X$ (and $X^TX$) isn't full rank, and hence $X^TX$ isn't invertible.


It's time to get started.