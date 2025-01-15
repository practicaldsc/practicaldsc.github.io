---
layout: page
title: 3. Matrices
description: >-
  Matrices and matrix-vector multiplication.
parent: 🧮 Linear Algebra
grand_parent: 🧑‍🤝‍🧑 Guides
nav_order: 3
---

# {{ page.title }}
{:.no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"> </script>

## Matrices and matrix-vector multiplication

<center>
<iframe width="800" height="225" src="https://www.youtube.com/embed/SqqmMRKwNw8?si=o7UBbbVEf0JgUM8i" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</center>

<small>
[📝 slides](../assets/7-matrices.pdf){: .btn } &nbsp; [🎥 video on YouTube](https://youtu.be/SqqmMRKwNw8){: .btn }
</small>

<details markdown="1">

<summary><b>Practice Questions 6.1-6.2</b></summary>

**Question 6.1**

Suppose $$M \in \mathbb{R}^{m \times n}$$ is a matrix, $$\vec{v} \in \mathbb{R}^n$$ is a vector, and $$s \in \mathbb{R}$$ is a scalar.

Determine whether each of the following quantities is a matrix, vector, scalar, or undefined. If the result is a matrix or vector, determine its dimensions.

**(a)** $$M\vec{v}$$

**(b)** $$\vec{v} M$$

**(c)** $$\vec{v}^2$$

**(d)** $$M^TM$$

**(e)** $$MM^T$$

**(f)** $$\vec{v}^T M \vec{v}$$

**(g)** $$(sM\vec{v}) \cdot (sM\vec{v})$$

**(h)** $$(s \vec{v}^T M^T)^T$$

**(i)** $$\vec{v}^T M^T M \vec{v}$$

**(j)** $$\vec{v}\vec{v}^T + M^TM$$

**(k)** $$\frac{M \vec{v}}{\lVert \vec{v} \rVert} + (\vec{v}^T M^T M \vec{v}) M \vec{v}$$

---

**Question 6.2**

Consider the matrix $$X$$ and vector $$\vec w$$ defined below:

$$X = \begin{bmatrix} 1 & 2 & 3 \\ 1 & 2 & 3 \\ 5 & 1 & -2 \end{bmatrix} \qquad \vec{w} = \begin{bmatrix} 4 \\ 3 \\ -1 \end{bmatrix}$$

**(a)** Evaluate $$X \vec{w}$$.

**(b)** As we learned in the video above, the matrix-vector product $$X \vec{w}$$ is a linear combination of the columns of the matrix, $$X$$, using weights from the vector $$\vec{w}$$.

Fill in each blank below with a single number from the start of Question 13.

$$X \vec{w} = \underline{\hspace{0.5cm}} \begin{bmatrix} \underline{\hspace{0.5cm}} \\ \underline{\hspace{0.5cm}} \\ \underline{\hspace{0.5cm}} \end{bmatrix} + \underline{\hspace{0.5cm}} \begin{bmatrix} \underline{\hspace{0.5cm}} \\ \underline{\hspace{0.5cm}} \\ \underline{\hspace{0.5cm}} \end{bmatrix} + \underline{\hspace{0.5cm}} \begin{bmatrix} \underline{\hspace{0.5cm}} \\ \underline{\hspace{0.5cm}} \\ \underline{\hspace{0.5cm}} \end{bmatrix}$$

**(c)** Let's generalize the idea from part (b). Now, suppose $$X \in \mathbb{R}^{n \times d}$$ is a matrix whose columns, $$\vec{x}^{(1)}, \vec{x}^{(2)}, ..., \vec{x}^{(d)}$$ are all vectors in $$\mathbb{R}^n$$, and suppose that $$\vec{w} \in \mathbb{R}^d$$.

Fill in the blanks:

$$X \vec{w} = \sum_{i = 1}^{\boxed{\:\:\:}} \boxed{\:\:\:}$$

**(e)** Evaluate $$X^TX$$ and $$XX^T$$.

</details>
