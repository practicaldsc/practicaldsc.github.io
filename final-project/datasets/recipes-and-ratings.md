---
layout: page
title: 🍽️ Recipes and Ratings
description: Description of the recipes and ratings dataset option for the Final Project.
nav_order: 1
grand_parent: 📊 Final Project
parent: 👨‍💻 Dataset Options
---

# {{ page.title }}
{:.no_toc}

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

This dataset contains recipes and ratings from [food.com](https://food.com). It was originally scraped and used by the authors of [this](https://cseweb.ucsd.edu/~jmcauley/pdfs/emnlp19c.pdf) recommender systems paper.

---

## Getting the Data

Download the data [here](https://drive.google.com/drive/folders/1bnnL1NBlLajrlP5E2Gw8Q72j9z2gbxsR?usp=sharing). You'll download two CSV files:
- `RAW_recipes.csv` contains recipes.
- `RAW_interactions.csv` contains reviews and ratings submitted for the recipes in `RAW_recipes.csv`.

We've provided you with a subset of the raw data used in the original report, containing only the recipes and reviews posted since 2008, since the original data is quite large.

A description of each column in both datasets is given below.

#### Recipes

For context, you may want to look at an example recipe [directly on food.com](https://www.food.com/recipe/chickpea-and-fresh-tomato-toss-51631).

| Column         | Description                                                                                                                                       |
|:---------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| `'name'`        | Recipe name                                                                                                                                       |
| `'id'`             | Recipe ID                                                                                                                                         |
| `'minutes'`        | Minutes to prepare recipe                                                                                                                         |
| `'contributor_id'` | User ID who submitted this recipe                                                                                                                 |
| `'submitted'`      | Date recipe was submitted                                                                                                                         |
| `'tags'`          | Food.com tags for recipe                                                                                                                          |
| `'nutrition'`      | Nutrition information in the form [calories (#), total fat (PDV), sugar (PDV), sodium (PDV), protein (PDV), saturated fat (PDV), carbohydrates (PDV)]; PDV stands for "percentage of daily value" |
| `'n_steps'`        | Number of steps in recipe                                                                                                                         |
| `'steps'`          | Text for recipe steps, in order                                                                                                                   |
| `'description'`    | User-provided description                                                                                                                         |

#### Ratings

| Column    | Description         |
|:----------|:--------------------|
| `'user_id'`   | User ID             |
| `'recipe_id'` | Recipe ID           |
| `'date'`      | Date of interaction |
| `'rating'`    | Rating given        |
| `'review'`    | Review text         |

{: .green }
> Beware: `RAW_recipes.csv` and `RAW_interactions.csv` are not the same size. `RAW_recipes.csv` has one row **per recipe**, but `RAW_interactions.csv` has one row **per review of a recipe**. So, a first step will be to combine the two datasets together in some informed way.
> - We think the most natural solution is to produce a combined DataFrame with one row **per recipe**. However, if you merge the two raw DataFrames together, you will not end up with just one row per recipe, but rather, one row per review of a recipe.
> - So, our advice is to group the interactions dataset by `'recipe_id'` and compute the average rating per recipe. This will yield a Series with one entry per recipe, which you can then add back to the recipes DataFrame by merging (or by adding it directly as a column, once you set the index of the recipes DataFrame to `'id'`). Then, if your goal is to predict ratings, what you'll really be predicting is average rating.
> - If you want to keep reviews along as well, you can group by `'recipe_id'` and sum the reviews column to once again yield a Series with one entry per recipe.

---

## Example Questions and Prediction Problems

Feel free to base your exploration into the dataset in Steps 1-2 around one of these questions, or come up with a question of your own.

- What types of recipes tend to have the most calories?
- What types of recipes tend to have higher average ratings?
- What types of recipes tend to be healthier (i.e. more protein, fewer carbs)?
- What is the relationship between the cooking time and average rating of recipes?

Feel free to use one of the prompts below to build your predictive model in Steps 3-5, or come up with a prediction task of your own.

- Predict ratings of recipes.
- Predict the number of minutes to prepare recipes.
- Predict the number of steps in recipes.
- Predict calories of recipes.

---

## Special Considerations

### Step 2: Data Cleaning and Exploratory Data Analysis

Some columns, like `'nutrition'`, contain values that look like lists, but are actually strings that look like lists. You may want to turn the strings into actual lists, or create columns for every unique value in those lists. For instance, per the data dictionary, each value in the `'nutrition'` column contains information in the form `"[calories (#), total fat (PDV), sugar (PDV), sodium (PDV), protein (PDV), saturated fat (PDV), and carbohydrates (PDV)]"`; you could create individual columns in your dataset titled `'calories'`, `'total fat'`, etc.