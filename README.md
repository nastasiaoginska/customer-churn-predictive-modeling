# Customer Churn Predictive Modeling

## Project Overview
This project presents an end-to-end, decision-oriented churn analysis for a subscription-based business.  
The goal is not only to predict customer churn, but to understand **why customers leave** and how predictive signals can support retention decisions.

## Business Problem
Customer churn represents a significant risk for subscription businesses, particularly during the early stages of the customer lifecycle.  
The objective of this project is to:

- estimate churn **probability** rather than binary churn labels,
- identify **high-risk customer segments**,
- support **risk ranking** for downstream retention strategies.

## Data & Features
The dataset consists of historical customer-level observations with a binary churn outcome.

Feature groups include:
- customer tenure,
- engagement metrics (logins, usage),
- satisfaction signals (NPS),
- payment behavior,
- pricing and plan information,
- regional and industry attributes.

All features are constructed using information available **prior to churn**, ensuring no target leakage.

## Methodology

### 1. Data Understanding & Preparation
- Exploratory analysis of churn distribution and feature behavior
- Data consistency checks and missing value handling
- Clear separation between data preparation and modeling stages

### 2. Feature Reasoning
- Univariate supervised segmentation using information gain
- Emphasis on behavioral and dynamic signals rather than static demographics
- Diagnostic analysis to inform modeling decisions (not automated feature selection)

### 3. Modeling
Two complementary modeling approaches are used.

#### Baseline Model — Logistic Regression
- Provides a stable probabilistic benchmark
- Optimized for churn risk ranking and calibration
- Used as the primary performance reference

#### Interpretable Model — Decision Tree
- Produces a supervised segmentation of the customer base
- Highlights key churn drivers and behavioral patterns
- Used for interpretability and business insight rather than predictive optimization

Models are evaluated using:
- ROC AUC
- Average Precision
- Log Loss
- Brier Score

## Key Findings
- **Customer tenure is the dominant driver of churn risk.**  
  Early-stage customers exhibit substantially higher churn probability.
- **Low engagement and low satisfaction are critical early warning signals**, especially within the first year.
- **Payment issues amplify churn risk primarily for newer customers**, while long-tenured customers remain resilient.
- Long-tenured customers form a **stable retention base** across most behavioral and pricing conditions.

## Business Implications
Retention efforts should prioritize:
- early-stage customers,
- onboarding quality and early engagement,
- proactive monitoring of satisfaction and payment friction.

For long-tenured customers, retention strategies can shift from prevention to value expansion.
