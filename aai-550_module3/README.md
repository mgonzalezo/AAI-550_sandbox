# 📊 Parametric vs. Non-Parametric Strategies in Nutrition Data Analysis

This project explores parametric and non-parametric statistical strategies using the **Daily Food & Nutrition Dataset**, with a specific focus on analyzing the distribution of **Sugars (g)**.

---

## 1. 📁 Dataset

- **Dataset Used:** Daily Food & Nutrition Dataset  
- **Source:** [Kaggle - Daily Food & Nutrition Dataset](https://www.kaggle.com/datasets/adilshamim8/daily-food-and-nutrition-dataset/data)

This synthetic dataset includes daily food and nutrition records covering macronutrients, micronutrients, food categories, and meal types.

---

## 2. 🎯 Project Goal

The goal of this project is to evaluate and demonstrate the differences between **parametric** and **non-parametric** statistical strategies in nutritional data analysis. 

We use the **Sugars (g)** variable as a case study to understand:
- When to apply each method
- What insights can be derived from both approaches
- How distribution shapes affect modeling decisions

---

## 3. 🛠️ Methodology Overview

The project follows these steps:

### ✅ Data Loading & Cleaning
- Load CSV data using pandas
- Convert relevant columns (e.g., Calories, Protein, Sugars) to numeric
- Remove rows with invalid or missing numerical values

### 📈 Exploratory Data Analysis (EDA)
- Use **histograms** and **Q-Q plots** to assess normality
- Analyze skewness and distribution shapes
- Use **box plots** to compare metrics like Calories across `Meal_Type`

### 🤖 Model Comparison (optional broader context)
- Applied **Linear Regression** (parametric) and **Random Forest Regressor** (non-parametric) to predict `Calories (kcal)`
- Though predictive accuracy was low, distributional insights remain relevant

---

## 4. 🍬 Evaluation of Sugars (g): Parametric vs. Non-Parametric

### 📊 Distribution Shape
- **Histogram** and **Q-Q Plot** of `Sugars (g)` reveal **highly skewed**, **non-normal** distribution
- Many low values, long right tail → violates assumptions of t-tests or ANOVA

### 🧠 Strategy Implications
- For inference involving `Sugars (g)`, use:
  - **Non-parametric tests** (e.g., Mann-Whitney U, Kruskal-Wallis)
  - **Transformations** or **robust models** when parametric analysis is necessary

---

## 5. 🔁 Bootstrapping Strategies Summary

Bootstrapping estimates uncertainty (e.g., sampling distribution, confidence intervals) by resampling. We demonstrate both approaches:

### 📐 Parametric Bootstrapping
- Assumes known distribution (e.g., Poisson, Normal)
- Example: `Sugars (g)` ~ Poisson(λ), where λ = sample mean
- ✅ **Pros:** Can simulate beyond observed values
- ❌ **Cons:** Misleading if model assumption is incorrect

### 🧪 Non-Parametric Bootstrapping
- No distribution assumption
- Samples directly with replacement from observed data
- ✅ **Pros:** Robust and data-driven
- ❌ **Cons:** Cannot simulate outside existing values; less flexible for extrapolation

---

## 6. 📤 Sharing Results

### 🔍 Visualizations
- Histograms and Q-Q plots show strong deviations from normality
- Box plots show variations across meal types
- These provide strong visual motivation for non-parametric approaches

### 🤖 Modeling Insights
- While predictive models (e.g., calorie estimation) didn't yield strong performance, they illustrate practical use of parametric vs non-parametric techniques in real-world nutrition data

---

## 📌 Conclusion

This project provides a reproducible example of:
- When to use parametric vs non-parametric strategies
- How to assess distribution shape in real data
- Why visual and statistical checks are critical in nutrition-based modeling

---

**Author:**  
[Your Name]  
**License:** MIT  
