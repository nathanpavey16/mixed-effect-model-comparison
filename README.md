## Overview

This project investigates whether accounting for group-level variation improves model performance when analysing panel data. Using a dataset of UK firms observed over multiple years, I compare fixed effects and mixed effects models to determine whether introducing random effects leads to improved explanatory and predictive performance.

The analysis demonstrates the balance between model complexity and predictive accuracy and highlights the importance of validating statistical models using predictive performance metrics.

## Objectives
Analyse longitudinal data on UK firms.

Compare fixed effects and mixed effects modelling approaches.

Evaluate whether firm-level heterogeneity improves model performance.

Assess model performance using cross-validation and holdout testing.

Demonstrate the use of statistical modelling to support evidence-based decision making.
## Dataset

The dataset contains annual observations for UK firms and includes:

Firm identifier

Year

Firm value

Capital

Investment

The firm variable is treated as a grouping factor, allowing both fixed and random effects specifications to be considered.

## Methodology
Exploratory Data Analysis

Visualised firm values over time.

Investigated differences in firm-specific trajectories.
## Fixed Effects Models

Baseline fixed effects model:

value ~ capital + year + inv + firm

Extended fixed effects model with firm-specific time trends:

value ~ capital + year + inv + firm + year:firm

## Mixed Effects Models

### Random intercept model:

value ~ year + capital + inv + (1 | firm)

### Random intercept and slope model:

value ~ year + capital + inv + (1 + year | firm)

## Model Evaluation

Models were compared using:

Adjusted (R^2)

Leave-One-Out Cross-Validation (LOOCV)

10-Fold Cross-Validation

Mean Squared Prediction Error (MSPE)

Likelihood Ratio Testing

Bayesian Information Criterion (BIC)

## Key Findings
The interaction model achieved a slightly higher in-sample fit but did not consistently improve predictive performance.

Introducing additional random effects increased model complexity without providing meaningful improvements in prediction accuracy.

The fixed effects model achieved the strongest predictive performance.
## Conclusion

This project demonstrates that more complex models do not necessarily lead to better predictions. Although mixed effects models would be expected to better fit the model, it is not always the case. The simpler fixed effects specification provided the most effective balance between explanatory power, predictive accuracy, and model parsimony for this dataset.

## Skills Demonstrated
Statistical Modelling

Linear Regression

Mixed Effects Models

Model Selection

Cross-Validation

Predictive Modelling

Data Visualisation

Statistical Inference

R Programming

## Tools
R

ggplot2

lme4

dplyr

tidyr

caret
