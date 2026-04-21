# Spotify Track Popularity Prediction with Statistical Learning

This project analyzes Spotify track-level audio features and genre information to study what drives track popularity and to build predictive models for popularity scores.

The work combines exploratory data analysis, statistical testing, feature-based modeling, and machine learning methods to understand the relationship between track characteristics and popularity.

## Project Overview

The analysis focuses on a Spotify dataset containing audio and metadata features such as:

- valence
- acousticness
- danceability
- explicit flag
- track genre
- loudness
- popularity

The project uses these features to:

1. explore trends and relationships in the dataset
2. test statistical patterns across genres and audio characteristics
3. build predictive models for popularity
4. compare regression-based and support vector methods
5. evaluate model performance using standard regression metrics

## Dataset Scope

- Original source material covered approximately 90,000 unique tracks across more than 100 genres
- The final statistical analysis focused on 10 popular genres for clearer comparison and modeling
- Popularity was modeled as the target variable on a 0 to 100 scale

## Methods and Tools

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Libraries:** pandas, numpy, matplotlib, seaborn, scipy, statsmodels, scikit-learn, tabulate
- **Modeling approaches:** linear regression, support vector regression, hyperparameter tuning with GridSearchCV
- **Evaluation metrics:** R-squared, mean squared error

## Statistical Findings

- Popularity differed significantly across genres based on the Kruskal-Wallis test
- Popularity also differed significantly between explicit and non-explicit tracks based on the Mann-Whitney test
- Genre and explicitness showed dependency in the chi-square analysis
- Acousticness showed a strong positive relationship with popularity
- Loudness showed a strong negative relationship with popularity
- Valence had only a weak relationship with popularity

## Model Results

| Model | R-squared | Mean Squared Error |
| --- | ---: | ---: |
| Multiple Linear Regression | 0.768 | 82.83 |
| Lasso Regression | 0.767 | 83.24 |
| Support Vector Regression | 0.742 | 92.33 |

The linear and lasso models performed best in the final comparison, while SVR captured similar directional effects but with lower overall predictive accuracy.

## Repository Structure

```text
spotify-track-popularity-prediction-statistical-learning/
  README.md
  .gitignore
  requirements.txt
  data/
    README.md
    raw/
      spotify-track-popularity-dataset.csv
  notebooks/
    spotify-track-popularity-prediction.ipynb
  reports/
    final-report.pdf
    final-presentation.pdf
    final-presentation.pptx
```

## Included Files

- `notebooks/spotify-track-popularity-prediction.ipynb`: final cleaned analysis notebook
- `data/raw/spotify-track-popularity-dataset.csv`: working dataset used in the project
- `reports/final-report.pdf`: final written report
- `reports/final-presentation.pdf`: presentation summary of the project
- `reports/final-presentation.pptx`: editable final presentation deck

## Main Conclusions

- Tracks with higher acousticness and lower loudness were more likely to be popular in this dataset
- Genre and explicitness were statistically important predictors and should not be ignored in modeling
- Multiple Linear Regression and Lasso Regression offered the best balance of interpretability and performance in the final project
- The project shows how statistical testing and machine learning can be combined in a practical music analytics workflow

## Notes

- The staged GitHub version keeps the final notebook and strongest supporting material.
- Draft notebooks and intermediate versions are intentionally excluded from the public repo.
- The notebook has been adjusted for repository-relative data access instead of Google Drive-only paths.
- The report and final presentation are the primary polished deliverables for this repository.
