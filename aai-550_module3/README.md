# Parametric vs. Non-Parametric Bootstrapping in Nutrition Data Analysis

This project explores parametric and non-parametric bootstrapping strategies using the [Daily Food & Nutrition Dataset](https://www.kaggle.com/datasets/adilshamim8/daily-food-and-nutrition-dataset/data), with a focus on the distribution of Sugars (g).

## 1. Dataset
- **Source:** Kaggle  
- **Description:** A synthetic dataset of daily food and nutrient intake, including meal types and macronutrient values like Calories and Sugars (g).

## 2. Project Goal
To demonstrate and compare how parametric and non-parametric bootstrapping approaches operate—highlighting their assumptions, implementation, and application to skewed nutritional data (e.g., Sugars).

## 3. Methodology
- **Data Cleaning:** Converted numeric columns, removed non-numeric or missing entries.
- **Distribution Assumption:** Simulated Poisson data as an example of a known parametric model.
- **Parametric Bootstrap:** Assumed Sugars (g) follows a Poisson(λ) distribution (λ = mean of observed values), and generated 1000 bootstrap means.
- **Non-Parametric Bootstrap:** Resampled the observed Sugars (g) data with replacement, also producing 1000 bootstrap means.
- **Visualization:** Compared histograms of the Poisson distribution and both bootstrapped sampling distributions.

## 4. Insights: Sugars (g)
- **Parametric Bootstrapping** works well if the model fits (e.g., Poisson), allowing extrapolation but risks inaccuracy if the assumption is off.
- **Non-Parametric Bootstrapping** requires no distributional assumption and better reflects the skewed, real-world distribution of Sugars (g).

## 5. Summary of Bootstrapping Methods

### Parametric
- Assumes known distribution (e.g., Poisson).
- **Pros:** Simulates unseen scenarios; useful for theory-driven inference.
- **Cons:** Misleading if the model is incorrect.

### Non-Parametric
- Resamples observed data.
- **Pros:** Robust to distributional assumptions.
- **Cons:** Limited to observed value ranges.

## 6. Conclusion
Visualizations highlight the differences between parametric and non-parametric bootstrapping. For skewed variables like Sugars (g), non-parametric methods offer a more data-driven and reliable approach to understanding variability and inference.

---
✅ For visual examples and code, refer to the Jupyter notebook in this repository.
