---
layout: page
title: Final Project 📊
description: Description of the Final Project, the final assignment of the semester.
nav_exclude: true
---

<script type="text/javascript" async="" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>

# Final Project 📊

{:.no_toc}

<!-- ### Checkpoint due Monday, November 25th at 11:59PM (no slip days allowed!)<br>Final Submission due Saturday, December 7th at 11:59PM (no slip days allowed!) -->

{:.no_toc}

- [Checkpoint](#checkpoint-submission) due **Friday, March 28th at 11:59PM** (slip days allowed!)
- Final Submission due **Tuesday, April 22nd at 11:59PM** (no slip days allowed!)

_last updated March 16 at 2:03PM_

---

Welcome to the Final Project, the final assignment of the semester! 👋

This project is a mini-homework of sorts, and aims to be a culmination of everything you've learned this semester. In the project, you will conduct an open-ended investigation into one of the three datasets (Recipes and Ratings 🍽, League of Legends ⌨️, or Power Outages 🔋), or – upon permission of the instructor – choose your own. **Specifically, you'll draw several visualizations to help understand the distributions of key variables, build and improve a predictive model, and share your findings with everyone on the internet.**

The Final Project is worth 100 points total; the breakdown is described in the [Rubric](#rubric) section at the bottom of this page. The Final Project is different from other homeworks in a few crucial ways:

- You **can work with one partner** (but don't have to). If you choose to work with a partner, read the [Partner Guidelines](#partner-guidelines) section at the bottom.
- There is a **checkpoint**, due March 28, 2025, worth 15 points out of the 100 points the project is scored out of. It exists to make sure you've picked a dataset and started some preliminary work. See the [Checkpoint Submission](#checkpoint-submission) section for more details and for the Gradescope submission link.
- You can use slip days on the checkpoint; however, you **cannot use slip days** on the final submission, since it's due so close to the end of the semester that we need all the time we can get to grade them. All components of the project are **manually graded**.
- You **cannot drop** the Final Project – it will be a part of your overall project grade no matter what. Your lowest score among Homeworks 1-11 will be the one that is dropped.
- As your final deliverables, you'll submit two things to us:
  - a **public-facing website**. We'll eventually create a public "showcase" site that has links to everyone's submissions – **that is, your website will be available to the entire internet!**
  - a **PDF of your Jupyter Notebook**.

Before we get into the details of what's expected of you, note that this project in particular is meant to encourage you to build something you're proud of. This is a chance to put something concrete on your resume to show potential employers. Grading will likely be lenient, but your work will be publicly available **forever**!

As alluded to above, the project is broken into two parts:

- Part 1: An **analysis**, submitted as a Jupyter Notebook. This will contain the details of your work. **Focus on completing your analysis before moving to Part 2, as the analysis is the bulk of the project.**
- Part 2: A **report**, submitted as a website. This will contain a narrative "story" with visuals. **Focus on this after finishing _most_ of your analysis.**

The project is worth a total of 100 points. You can see the distribution of points in the [Rubric](#rubric) section at the very bottom.

---

## Table of Contents

<!-- {: .no_toc .text-delta }

1. TOC
   {:toc} -->

{:text-delta}
{:toc}

---

## Choosing a Dataset

In this project, you will perform an open-ended investigation into a **single dataset**.

### Default Options

We expect that the majority of students will choose **one** of the following three datasets.

[Recipes and Ratings 🍽](recipes-and-ratings){: .btn } &nbsp;&nbsp; [League of Legends ⌨️](league-of-legends){: .btn } &nbsp;&nbsp; [Power Outages 🔋](power-outages){: .btn }

The dataset description pages linked above each have three sections:

- **Getting the Data**: Describes how to access the data and, in some cases, what various features mean. (In general, you're going to have to understand what your data means on your own!) **You're welcome to download additional data to help with your analyses, in addition to using the data that's provided for you.**
- **Example Questions and Prediction Problems**: Use these as inspiration, but feel free to come up with your own questions and prediction problems!
- **Special Considerations**: Things to be aware of when working with the given dataset, e.g. some additional requirements.

When selecting which dataset you are going to use for your project, try choosing the one whose topic appeals to you the most as that will make finishing the project a lot more enjoyable.

To help contextualize the kinds of analysis you can do in this project, it might help to look at these examples from a last semester's (FA24) [Showcase Page](https://practicaldsc.org/showcase/), which were formerly known as the "Portfolio Homework." These examples offer insights into crafting effective research questions, but bear in mind that they have their own strengths and weaknesses. Treat them as a foundation for inspiration, but **don't** just repeat or copy their work - be original!

1. [What Causes Severe Outages?](https://andregalagarza.github.io/power-outage-analysis/): This project presents a noval way to do the data visualization. In your project, please think about what is the best way to present your data.

2. [Cooking Time, Calories, and Ratings: The Secret Ingredients of Recipe Success](https://jpswag.github.io/recipes-and-ratings/): This project clearly outlines how to address data quality challenges. In your own project, ensure that you document your data cleaning process and provide clear justifications for your decisions.

3. [How big is League of Lengends snowball effect?](https://naouyang.github.io/2022-league-of-legends-analysis/): This project excelled in clarifying their research aims, making the study understandable to a broader audience. In your own project, ensure that you provide a lucid and detailed explanation of your research focus.

<!-- To help contextualize the kinds of analysis you can do in this project, it might help to look at these examples from a related course taught at UC San Diego. These examples offer insights into crafting effective research questions, but bear in mind that they have their own strengths and weaknesses. Treat them as a foundation for inspiration, but **don't** just repeat or copy their work – be original! Also note that the UC San Diego version of this assignment had slightly more requirements, so you'll see sections involving (for example) hypothesis tests that you aren't expected to have.

1. [League of Legends First Blood Statistical Analysis](https://krystalqjx.github.io/LOL-analysis/): This homework excelled in clarifying their research aims, making the study understandable to a broader audience. In your own project, ensure that you provide a lucid and detailed explanation of your research focus.
2. [Analyzing Power Outages](https://nghosh24.github.io/power-outages/): This project presents a noval way to do the data visualization. In your project, please think about what is the best way to present your data. -->

{: .green }
Before choosing a dataset, read the rest of this page to see what's required of you!

### Choosing Your Own Dataset

You may not be interested in any of the above datasets, or may already be doing research/other work involving a dataset that is of particular interest to you. If that's the case, you _may_ be permitted to use a different dataset. You can take a look at our [resources](https://practicaldsc.org/resources/#finding-datasets) for finding datasets if there’s another topic you’re interested in. **To request approval**, send Suraj (rampure@umich.edu) an email with answers to the following questions:

1. Why do you want to work with this dataset over the default options?
2. What preliminary research questions do you plan to address with this dataset?
3. Which features in the dataset do you consider key to your initial analysis and why?
4. What feature do you plan to predict, and what features do you anticipate using in your predictive model?
5. What is the size of the dataset (number of observations and features)?
6. Is there missing data? If so, how do you plan on handling it?
7. Please provide a link / attach the dataset.

**The deadline to request approval to use a different dataset is before the deadline for the checkpoint. You must email Suraj by Wednesday, March 26th.** Once you email Suraj with the above, you should hear back within 48 hours with your approval or denial and reasoning. Note that submitting the checkpoint is not the same as requesting approval; the only way to request approval to use a different dataset is to email Suraj with answers to the questions above. After **March 26th**, if you haven't requested approval, you **must** choose one of the default three options.

Below is an example of a custom dataset Final Project from last semester's (FA24) [Showcase Page](https://practicaldsc.org/showcase/). Again, use these projects as inspiration when designing your own analysis with a custom dataset:

1. [Trip Times and Trends](https://dgraham6.github.io/Taxi-EDA/): This project effectively creates new, insightful features that capture underlying patterns. In your own project, think creatively to derive features that add predictive value where applicable.

---

## Part 1: Analysis

Before beginning your analysis, you'll need to set up a few things.

1. Pull the latest version of the course GitHub repo, [github.com/practicaldsc/wn25](https://github.com/practicaldsc/wn25). Within the `homeworks/final-project` folder, there is a `template.ipynb` notebook that you will use as a template for the project. If you delete the file or want another copy of the template, you can re-download it from [here](https://github.com/practicaldsc/wn25/blob/main/homeworks/final-project/template.ipynb). **This is where your analysis will live; you will submit this entire notebook to us.**
1. Download the [dataset](#choosing-a-dataset) you chose and load it into your template notebook.

Once you have your dataset loaded in your notebook, it's time for you to find meaning in the real-world data you've collected! Follow the steps below.

{: .green }
For each step, we specify what must be done in your notebook and what must go on your website, which we expand on in [Part 2](#part-2-report). We recommend you write everything in your notebook first, and then move things over to your website once you've completed your analysis.

<br>

In Steps 1-2, you'll develop a deeper understanding of your dataset while trying to answer a single question.

### Step 1: Introduction

| Step                                         | Analysis in Notebook                                                                                                                                                                                                                                                                                                                  | Report on Website                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Introduction and Question Identification** | Understand the data you have access to. Brainstorm a few questions that interest you about the dataset. Pick **one** question you plan to investigate further. (As the [data science lifecycle](https://practicaldsc.org/resources/lectures/lec01/lec01.html#Topics) tells us, this question may change as you work on your project.) | Provide an introduction to your dataset, and clearly state the one question your project is centered around. Why should readers of your website care about the dataset and your question specifically? Report the number of rows in the dataset, the names of the columns that are relevant to your question, and descriptions of those relevant columns. |

### Step 2: Data Cleaning and Exploratory Data Analysis

| Step                       | Analysis in Notebook                                                                                                                                                                                                                                                 | Report on Website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Data Cleaning**          | Clean the data appropriately. For instance, you may need to replace data that should be missing with `NaN` or create new columns out of given ones (e.g. compute distances, apply numerical-to-numerical transformations, or get time information from time stamps). | Describe, in detail, the data cleaning steps you took and how they affected your analyses. The steps should be explained in reference to the data generating process. Show the `head` of your cleaned DataFrame (see [Part 2: Report](#part-2-report) for instructions).                                                                                                                                                                                                                                                                                                                       |
| **Univariate Analysis**    | Look at the distributions of relevant columns separately by using DataFrame operations and drawing at least two relevant plots.                                                                                                                                      | Embed **at least one** `plotly` plot you created in your notebook that displays the distribution of a single column (see [Part 2: Report](#part-2-report) for instructions). Include a 1-2 sentence explanation about your plot, making sure to describe and interpret any trends present, and how they answer your initial question. (Your notebook will likely have more visualizations than your website, and that's fine. Feel free to embed more than one univariate visualization in your website if you'd like, but make sure that each embedded plot is accompanied by a description.) |
| **Bivariate Analysis**     | Look at the statistics of pairs of columns to identify possible associations. For instance, you may create scatter plots and plot conditional distributions, or box plots. You must plot at least two such plots in your notebook. Be creative!                      | Embed **at least one** `plotly` plot that displays the relationship between two columns. Include a 1-2 sentence explanation about your plot, making sure to describe and interpret any trends present and how they answer your initial question. (Your notebook will likely have more visualizations than your website, and that's fine. Feel free to embed more than one bivariate visualization in your website if you'd like, but make sure that each embedded plot is accompanied by a description.)                                                                                       |
| **Interesting Aggregates** | Choose columns to group and pivot by and examine aggregate statistics.                                                                                                                                                                                               | Embed at least one grouped table or pivot table in your website and explain its significance.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Imputation**             | If needed for further analyses, impute any missing values.                                                                                                                                                                                                           | If you imputed any missing values, visualize the distributions of the imputed columns before and after imputation. Describe which imputation technique you chose to use and why. If you didn't fill in any missing values, discuss why not.                                                                                                                                                                                                                                                                                                                                                    |

<br>

In Steps 3-5, you will build a predictive model, based on the knowledge of your dataset you developed in Steps 1-2.

### Step 3: Framing a Prediction Problem

| Step                       | Analysis in Notebook                                                                                                                                                                                                                                                                                                                                                                                       | Report on Website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Problem Identification** | Identify a prediction problem. Feel free to use one of the example prediction problems stated in the "Example Questions and Prediction Problems" section of your dataset's description page or pose one of your own. The prediction problem you come up with doesn't have to be related to the question you were answering in Steps 1-2, but ideally, your entire project has some sort of coherent theme. | Clearly state your prediction problem and type (classification or regression). If you are building a classifier, make sure to state whether you are performing binary classification or multiclass classification. Report the response variable (i.e. the variable you are predicting) and why you chose it, the metric you are using to evaluate your model and why you chose it over other suitable metrics (e.g. accuracy vs. F1-score).<br><br>**_Note_**: Make sure to justify what information you would know at the "time of prediction" and to only train your model using those features. For instance, if we wanted to predict your Final Exam grade, we couldn’t use your Final Project grade, because we (probably) won't have the Final Project graded before the Final Exam! Feel free to ask questions if you're not sure. |

### Step 4: Baseline Model

| Step               | Analysis in Notebook                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Report on Website                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Baseline Model** | Train a "baseline model" for your prediction task that uses at least two features. (For this requirement, two features means selecting at least two unique columns from your original dataset.) You can leave numerical features as-is, but you'll need to take care of categorical columns using an appropriate encoding. Implement all steps (feature transforms and model training) in a single `sklearn` Pipeline. <br><br>**_Note_**: **Both now and in Step 5: Final Model, make sure to evaluate your model's ability to generalize to unseen data!** <br><br>There is no "required" performance metric that your baseline model needs to achieve. | Describe your model and state the features in your model, including how many are quantitative, ordinal, and nominal, and how you performed any necessary encodings. Report the performance of your model and whether or not you believe your current model is "good" and why.<br><br>**_Tip_**: Make sure to hit all of the points above: many Final Projects in the past have lost points for not doing so. |

### Step 5: Final Model

| Step            | Analysis in Notebook                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Report on Website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Final Model** | Create a "final" model that improves upon the "baseline" model you created in Step 4. Do so by engineering at least two new features from the data, on top of any categorical encodings you performed in Baseline Model Step. (For instance, you may use a `StandardScaler` on a quantitative column and a `QuantileTransformer` transformer on a different column to get two new features.) Again, implement all steps in a single `sklearn` Pipeline. While deciding what features to use, you **must** perform a search for the best hyperparameters (e.g. tree depth) to use amongst a list(s) of options, either by using `GridSearchCV` or through some manual iterative method. In your notebook, state which hyperparameters you plan to tune and why before actually tuning them.<br><br>**_Optional_**: You are encouraged to try many different modeling algorithms for your final model (i.e. `LinearRegression`, `RandomForestClassifier`, `Lasso`, `SVC`, etc.) If you do this, make sure to clearly indicate in your notebook which model is your actual final model as that will be used to grade the above requirements.<br><br>**_Note 1_**: When training your model, make sure you use the same training and testing sets from your baseline model. This way, the evaluation metric you get on your final model can be compared to your baseline's on the basis of the model itself and not the dataset it was trained on. Based on which method you use for hyperparameter tuning, this may mean that you will need to use some of your training data as your validation data. If this is the case, make sure to train your final model on the whole training set to evaluation.<br><br>**_Note 2_**: You will not be graded on "how much" your model improved from Step 4: Baseline Model to Step 5: Final Model. What you will be graded on is on whether or not your model improved, as well as your thoughtfulness and effort in creating features, along with the other points above.<br><br>**_Note 3_**: Don't try to improve your model's performance just by blindly transforming existing features into new ones. Think critically about what each transformation you're doing actually does. For example, there's no use in using a `StandardScaler` transformer if your goal is to reduce the MSE of a linear model: as we learned in Lecture 18, standardizing features in a regression model does not change the model's predictions, only its coefficients! | State the features you added and **why** they are good for the data and prediction task. Note that you can't simply state "these features improved my accuracy", since you'd need to choose these features and fit a model before noticing that – instead, talk about _why_ you believe these features improved your model's performance from the perspective of the data generating process. <br><br>Describe the modeling algorithm you chose, the hyperparameters that ended up performing the best, and the method you used to select hyperparameters and your overall model. Describe how your Final Model's performance is an improvement over your Baseline Model's performance.<br><br>**_Optional_**: Include a visualization that describes your model's performance, e.g. a confusion matrix, if applicable. |

### Style

While your website will be neatly organized and tailored for public consumption, it is important to keep your analysis notebook organized as well. Follow these guidelines:

- Your work for each of the five project steps described above (Introduction, Data Cleaning and Exploratory Data Analysis, ..., Final Model) should be completed in code cells underneath the Markdown header of that section's name.
- You should **only include work that is relevant** to posing, explaining, and answering the question(s) you state in your website. You should include data quality, cleaning, and missingness assessments, and intermediate models and features you tried, though these should broadly be relevant to the tasks at hand.
- Make sure to clearly explain what each component of your notebook **means**. Specifically:
  - All plots should have titles, labels, and a legend (if applicable), even if they don't make it into your website. Plots should be self-contained – readers should be able to understand what they describe without having to read anything else.
  - All code cells should contain a comment describing how the code works (unless the code is self-explanatory – use your best judgement).

---

## Part 2: Report

Your website is the public-facing component of your Final Project. While GitHub Pages (specifically [Jekyll](https://jekyllrb.com), a framework built into GitHub Pages that allows you to create professional-looking websites just by writing Markdown is the easiest and free option for hosting a static website, you are not limited to this approach. In fact, [practicaldsc.org](https://practicaldsc.org) is built using Jekyll!. GitHub Pages does the "hard" part of converting your Markdown to HTML.), a framework built into GitHub Pages

If you wish to build a dynamic website, consider frameworks like Streamlit or Marimo. Dynamic websites allow you to incorporate interactive elements and real-time data updates. However, for simplicity and ease of maintenance, many students choose GitHub Pages. Ultimately, you can host your website however you want—as long as your final submission includes a link that is publicly accessible.

The purpose of your website is to provide the general public – your classmates, friends, family, recruiters, and random internet strangers – with an overview of your project and its findings, without forcing them to understand every last detail. We don't expect the website creation process to take very much time, but it will certainly be rewarding. Once you've completed your analysis and know _what_ you will put in your website, start reading this section.

Your website must clearly contain the following five headings, corresponding to the five steps mentioned in [Part 1](#part-1-analysis):

- Introduction
- Data Cleaning and Exploratory Data Analysis
- Framing a Prediction Problem
- Baseline Model
- Final Model

**Don't** include "Step 1", "Step 2", etc. in your headings – the headings should be exactly as they are above.

The specific content your website needs to contain is described in the "Report on Website" columns above. **Make sure to also give your website a creative title that relates to the question you're trying to answer, and clearly state your name(s) and email(s).**

<!-- Your report will be in the form of a _static_ website, hosted for free on GitHub Pages. More specifically, you'll use [Jekyll](https://jekyllrb.com), a framework built into GitHub Pages that allows you to create professional-looking websites just by writing Markdown ([practicaldsc.org](https://practicaldsc.org) is built using Jekyll!). GitHub Pages does the "hard" part of converting your Markdown to HTML. -->

If you'd like to follow the official [GitHub Pages & Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll) tutorial, you're welcome to, though we will provide you with a perhaps simpler set of instructions here. A very basic site with an embedded visualization can be found at [rampure.org/dsc80-proj3-test1/](http://rampure.org/dsc80-proj3-test1/); the source code for the site is [here](https://github.com/surajrampure/dsc80-proj3-test1). Note that this example site doesn't have the same headings that you're required to have.

### Step 1: Initializing a Jekyll GitHub Pages Site

1. Create a GitHub account, if you don't already have one.
1. Create a new GitHub repository for your project. Give it a descriptive name, like `league-of-legends-analysis`, not `eecs398-portfolio-hw`.
   - GitHub Pages sites live at `<username>.github.io/<reponame>` (for instance, the site for [github.com/practicaldsc.org/wn25](https://github.com/practicaldsc/wn25) is [practicaldsc.github.io/wn25](https://practicaldsc.github.io/wn25), which we redirect to from [practicaldsc.org](https://practicaldsc.org)).
   - As such, **don't** include "EECS 398" or "Final Project" in your repo's name – this looks unprofessional to future employers, and gives you a generic-sounding URL. Instead, mention that this is a project for EECS 398 at U-M in the repository description.
   - **Make sure to make your repository public.**
   - Select "ADD a README file." This ensures that your repository starts off non-empty, which is necessary to continue.
1. Click "Settings" in the repository toolbar (next to "Insights"), then click "Pages" in the left menu.
1. Under "Branch", click the "None" dropdown, change the branch to "main", and then click "Save." You should soon see "GitHub Pages source saved." in a blue banner at the top of the page. This initiates GitHub Pages in your repository.
1. After 30 seconds, reload the page again. You should see "**Your site is live at http://username.github.io/reponame/**". Click that link – you now have a site!
1. Click "Code" in the repo toolbar to return to the source code for your repo.

Note that the source code for your site lives in `README.md`. **As you push changes to `README.md`, they will update on your site automatically within a few minutes!** Before moving forward, make sure that you can make basic edits:

1. Clone your repo locally.
1. Make some edits to `README.md`.
1. Push those changes back to GitHub, using the following steps:
   - Add your changes to "staging" using `git add README.md` (repeat this for any other files you add).
   - Commit your changes using `git commit -m '<some message here>'`, e.g. `git commit -m 'changed title of website'`.
   - Push your changes using `git push`.

Moving forward, we recommend making edits to your website source code locally, rather than directly on GitHub. This is in part due to the fact that you'll be creating folders and adding files to your source code.

### Step 2: Choosing a Theme

The default "theme" of a Jekyll site is not all that interesting.

To change the theme of your site:

1. Create a file in your repository called `_config.yml`.
1. Go [here](https://pages.github.com/themes/), and click the links of various themes until you find one you like.
1. Open the linked repository for the theme you'd like to use and scroll down to the "Usage" section of the README. Copy the necessary information from the README to your `_config.yml` and push it to your site.

For instance, if I wanted to use the Merlot theme, I'd put the following in my `_config.yml`:

```yml
remote_theme: pages-themes/merlot@v0.2.0
plugins:
  - jekyll-remote-theme # add this line to the plugins list if you already have one
```

Note that you're free to use any Jekyll theme, not just the ones that appear [here](https://pages.github.com/themes/). You are required to choose _some_ theme other than the default, though. See more details about themes [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll).

### Step 3: Embedding Content

Now comes the interesting part – actually including content in your site. The [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/) contains tips on how to format text and other page components in Markdown (and if you'd benefit by seeing an example, you could always look at the Markdown source of [this very page](https://raw.githubusercontent.com/practicaldsc/practicaldsc.github.io/refs/heads/main/final-project/index.md) – meta!).

### Embedding Interactive Plotly Visualizations

What will be a bit trickier is embedding `plotly` plots in your site so that they are interactive. Note that you are **required** to do this, you cannot simply take screenshots of plots from your notebooks and embed them in your site. Here's how to embed a `plotly` plot directly in your site.

1. **Export Your Plot to HTML:**
   First, you'll need to convert your plot to HTML. If `fig` is a `plotly` `Figure` object (for instance, the result of calling `px.express`, `go.Figure`, or `.plot` when `pd.options.plotting.backend = "plotly"` has been run), then the method `fig.write_html` saves the plot as HTML to a file. Call it using `fig.write_html('file-name.html', include_plotlyjs='cdn')`.
   - Change `'file-name.html'` to the path where you'd like to initially save your plot.
   - `include_plotlyjs='cdn'` tells `write_html` to load the source code for the `plotly` library from a server, rather than including the entire source code in your HTML file. This drastically reduces the size of the resulting HTML file, keeping your repo size down.
1. **Move the HTML File:**
   Move the `.html` file(s) you've created into a folder in your website repo called `assets` (or something similar).
   - Depending on where your template notebook is saved, you could combine this step with the step above by calling `fig.write_html` with the correct path (e.g. `fig.write_html('../league-match-analysis/assets/matches-per-year.html')).
1. **Embed the Plot in Your Markdown:**
   In `README.md`, embed your plot using the following syntax:

```html
<iframe
  src="assets/file-name.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>
```

- `iframe` stands for "inline frame"; it allows us to embed HTML files within other HTML files.
- You can change the `width` and `height` arguments, but don't change the `frameBorder` argument.

Refer [here](https://rampure.org/dsc80-proj3-test1/#assessment-of-missingness) for a working example (and [here](https://github.com/surajrampure/dsc80-proj3-test1) for its source code).

{: .note }
Try your best to make your plots look professional and unique to your group – add axis labels, change the font and colors, add annotations, etc. Remember, potential employers will see this – you don't want your plots to look like everyone else's! If you'd like to match the styles of the `plotly` plots used in lecture (e.g. with the white backgrounds), you can import and use the `lec_utils.py` file that's in the `homeworks/portfolio` folder of our public repo, alongside `template.ipynb`.

### Embedding Tables

- **Direct Markdown Tables:**
  To convert a DataFrame in your notebook to Markdown source code (which you need to do for both the **Data Cleaning** and **Interesting Aggregates** sections of Step 2: Data Cleaning and Exploratory Data Analysis in Part 1), use the `.to_markdown()` method on the DataFrame. For instance,

```py
print(counts[['semester', 'Count']].head().to_markdown(index=False))
# Output looks something like:
| semester    | Count |
|-------------|-------|
| Fall 2020   | 3     |
| Winter 2021 | 2     |
| Spring 2021 | 6     |
| Summer 2021 | 4     |
| Fall 2021   | 55    |

```

displays a string, containing the Markdown representation of the first 5 rows of `counts`, including only the `'semester'` and `'Count'` columns (and not including the index). You can see how this appears [here](http://rampure.org/dsc80-proj3-test1/#assessment-of-missingness); remember, no screenshots (and also remember that the "Assessment of Missingness" title is not something you need to have, that's just an example website). You may need to play with this a little bit so that you don't show DataFrames that are super, super wide and look ugly.

- **Embedding Pre-rendered Tables:**
  For larger or more complex tables, you can export them as an HTML file or as an image:
  - HTML: Embed via an <iframe> similar to Plotly plots:

```html
<iframe src="assets/table.html" width="800" height="400" frameborder="0">
</iframe>
```

- Image: Embed the table image using Markdown:

```markdown
![Table Description](assets/table.png)
```

### Local Setup

The above instructions give you all you need to create and make updates to your site. However, you _may_ want to set up Jekyll locally, so that you can look at how changes to your site would look without having to push and wait for GitHub to re-build your site. To do so, follow the steps [here](https://jekyllrb.com/docs/installation/) and then [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).

### Windows

Using RubyInstaller for Windows:

1. **Install Ruby and Devkit:**
   - Download a Ruby+Devkit version (RubyInstaller-2.4 or newer) from the [RubyInstaller Downloads](https://rubyinstaller.org/downloads/). If you're not sure which version to choose, use the Ruby+Devkit 3.3.X (x64) installer—the bolded option starting with **=>**.
   - Use the default installation options.
   - In the final step of the installer, run the `ridk install` command and choose the "MSYS2 and MINGW development toolchain" option. This is necessary for building native extensions when installing gems.
1. **Set Up Your Environment:**
   - Open a new Command Prompt window (this ensures your udpated PATH is active).
1. **Install Jekyll and Bundler:**
   - Run the following command to install Jekyll and Bundler:
   ```bash
   gem install jekyll bundler
   ```
   - Verify the installation with:
   ```bash
   jekyll -v
   ```
   - If an error occurs, reboot your system and try again.
   - If you want to use Windows Subsystem for Linux (WSL), please consult [Installation via Bash on Windows 10](https://jekyllrb.com/docs/installation/windows/#installation-via-bash-on-windows-10).

#### macOS

1. **Install Homebrew:**
   - Open Terminal and run:
   ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
1. **Install a Ruby Version Manager:**
   - Install **chruby** and **ruby-install** using Homebrew:
   ```bash
     brew install chruby ruby-install
   ```
1. **Install a Newer Ruby Version:**
   - Install the latest stable version of Ruby (e.g., 3.4.1) with:
     ```bash
     ruby-install ruby 3.4.1
     ```
   - Configure your shell by adding these lines to your configuration file (e.g., `~/.zshrc` for Zsh or `~/.bash_profile` for Bash):
     ```bash
     source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh
     source $(brew --prefix)/opt/chruby/share/chruby/auto.sh
     echo "chruby ruby-3.4.1" >> ~/.zshrc
     ```
   - Quit and relaunch Terminal, then verify by running:
     ```bash
     ruby -v
     ```
     It should display Ruby 3.4.1 (or a newer version).
1. **Install Jekyll and Bundler:**
   - With the new Ruby version active, run:
     ```bash
     gem install jekyll bundler
     ```

#### [Building your site locally](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#building-your-site-locally)

1. **Open Git Bash** (your terminal with Git installed).
1. **Navigate to Your Site's Publishing source:**
   - `cd` into your root folder where your Jekyll files (including `_config.yml`) are located.
1. **Install Dependencies with Bundler:**
   - Make sure you have a `GemFile` in your site's root directory that lists all required gems (like Jekyll and any plugins).
   - Run the following command to install all dependencies:
   ```
   bundle install
   ```
   - This command reads your `Gemfile` and installs the necessary Ruby gems.
1. **Serve Your Jekyll Site Locally:**
   - To build your site and start a local web server, run:
   ```
   bundle exec jekyll serve
   ```
   - This command performs several tasks:
     - Reads your `_config.yml` file.
     - Builds your site into the `_site` directory.
     - Starts a local server (usually at `http://127.0.0.1:4000/`) with auto-regeneration enabled, so your site rebuilds when you make changes.
   - Open your web browser and go to `http://localhost:4000` to preview your site.

{: .red }

> If, after running the above steps, running `bundle exec jekyll serve` in your local website repository doesn't work, then follow these steps.
>
> 1. In your Terminal, `cd` to your local website repository (folder).
> 1. Run `bundle init` to create a Gemfile (a file that specifies which Ruby extensions your project needs).
> 1. Open the Gemfile created in your local repository, delete everything that's currently there, and replace it all with:

```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
```

> 1. Run `bundle install` and then `bundle exec jekyll serve`.
>    If, after that, you still can't render your site locally, let us know what error `bundle exec jekyll serve` throws for you and we'll try and troubleshoot! Or, checkout [Troublshooting](https://jekyllrb.com/docs/troubleshooting/) to see if your questions have already been answered.

---

## Submission and Rubric

Overall, the homework is worth 100 points. We describe the breakdown in the [Rubric](#rubric) section below.

### Checkpoint Submission

As mentioned at the top of this page, this project has a required checkpoint, worth **15 of the 100 points**. You can submit the checkpoint [**here**](https://www.gradescope.com/courses/823979/assignments/5267579) on Gradescope. The checkpoint asks you to answer the following questions:

1. (3 points) Which of the three datasets did you choose and why? Or did you get pre-approval to choose your own dataset, and why?
1. (6 points) Upload a screenshot of a `plotly` visualization you've created while completing Part 1, Step 2: Data Cleaning and Exploratory Data Analysis.
1. (6 points) What is the column you plan on trying to predict in Part 1, Steps 3-5? Is it a classification or regression problem?

### Final Submission

You will ultimately submit your project in two ways:

1. By uploading a **PDF version** of your notebook to the specific "Final Project Notebook PDF (Dataset)" assignment on Gradescope **for your dataset**.
   - To export your notebook as a PDF, first, restart your kernel and run all cells. Then, go to "File > Print Preview". Then, save a print preview of the webpage as a PDF. There are other ways to save a notebook as a PDF but they may require that you have additional packages installed on your computer, so this is likely the most straightforward.
   - It's fine if your `plotly` graphs don't render in the PDF output of your notebook. However, **make sure none of the code is cut off in your notebook's PDF**. **You will lose 5% of the points available on this project if your code is cut off.**
   - This notebook asks you to include a link to your website; make sure to do so.
2. By submitting a **link to your website** to the "Final Project Website Link (All Datasets)" assignment on Gradescope.
   - We will use the links provided on Gradescope to create a "showcase site" with links to everyone's websites so that the rest of the class can see your work!
   - Here, you'll also need to provide your group member name(s), email(s), and the title of your website.

To both submissions, make sure to tag your partner. You don't need to submit your actual `.ipynb` file anywhere. **While your website must be public and you should share it with others, you should _not_ make your code for this project available publicly.**

{: .warning }
Remember that you can't use slip days on any part of this project – not on the checkpoint, not on the final PDF submission, and not on the final website link submission. There are a lot of moving parts to this assignment – don't wait until the last minute to try and submit!

### Rubric

Your project will be graded out of 100 points. The rough rubric is shown below. If you satisfy these requirements as described above, you will receive full credit.

Note that the rubric is intentionally vague when it comes to Steps 3-5. This is because an exact rubric would specify exactly what you need to do to build a model, but figuring out what to do is a large part of Steps 3-5.

| Component                                                                                                                                                                                                                                            | Weight         |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| **Checkpoint**                                                                                                                                                                                                                                       | 15 points      |
| **Step 1: Introduction**                                                                                                                                                                                                                             | 5 points       |
| **Step 2: Data Cleaning and Exploratory Data Analysis** <br>• Cleaned data (5 points)<br>• Performed univariate analyses (5 points)<br>• Performed bivariate analyses and aggregations (5 points)<br>• Commented on imputation strategies (5 points) | 20 points      |
| **Step 3: Framing a Prediction Problem**                                                                                                                                                                                                             | 5 points       |
| **Step 4: Baseline Model**                                                                                                                                                                                                                           | 20 points      |
| **Step 5: Final Model**                                                                                                                                                                                                                              | 25 points      |
| **Overall: Included all necessary components on the website**                                                                                                                                                                                        | 10 points      |
| **Total**                                                                                                                                                                                                                                            | **100 points** |

---

## Partner Guidelines

Working with a partner? Keep the following points in mind:

1. You are both required to actively contribute to all parts of the project. You must both be working on the assignment at the same time together, either physically or virtually on a Zoom call. You are encouraged to follow the **pair programming model**, in which you work on just a single computer and alternate who writes the code and who thinks about the problems at a high level. **In particular, you cannot split up the project and each work on separate parts independently.** So, you **cannot** say Partner 1 is responsible for the analysis and Partner 2 is responsible for the website.
1. You should decide on your partnership as soon as possible, but certainly before the checkpoint deadline of March 28th (which you're required to submit on your own).
1. Ultimately, you will submit three deliverables for this project to three separate Gradescope assignments – the checkpoint, a PDF of your notebook, and a link to your website. **Make sure to have just one partner submit these deliverables, and have them tag the other partner!** That is, don't make duplicate submissions of the same work.

## Frequently Asked Questions (FAQs)

### How should I decide between regression and classification for my model?

A useful heuristic when designing your model is to decide whether your variables should be treated as continuous or as categorical. Ask yourself:

- **Can you measure the difference between the maximum and minimum values quantitatively?**  
  If you can, then a regression model is appropriate because it captures incremental differences and predicts precise numerical outcomes.

- **Or, is the distinction between high and low values more qualitative—where the maximum is simply "better" or "more" than the minimum?**  
  In this case, a classification model might be more suitable, as it groups outcomes into distinct categories.

This approach helps ensure that your model reflects the true nature of your data. For a deeper discussion on this topic, see this [Stack Exchange discussion](https://stats.stackexchange.com/questions/68834/what-is-the-benefit-of-breaking-up-a-continuous-predictor-variable).

### Can I use dynamic website frameworks instead of GitHub Pages?

Yes! Although [GitHub Pages](https://github.com) using [Jekyll](https://jekyllrb.com) is the easiest and free option for hosting a static site, you can also choose to build a dynamic website using frameworks like Streamlit or Marimo. The key requirement is that your website must be publicly accessible for your final submission.

### How Should I Organize My Assets?

Keep all images, HTML files, and other assets in a dedicated folder (e.g., `assets`) within your repository. This practice helps maintain a clean project structure and makes it much easier to update or locate files later.

### How Do I Decide Between Interactive and Static Visualizations?

Use interactive visualizations when you want to allow users to explore the data in real time. For simpler displays or when interactivity is not essential, static images are a great alternative. Choose the method that best suits your data and the story you wish to tell.

### How Can I Ensure My Visualizations Are Consistent?

Ensure that every visualization you include has clear titles, axis labels, and legends. This makes each plot self-contained and easy for viewers to understand without needing extra context.
