# Interpretable Prediction of Geopolymer Concrete Compressive Strength Using DBO-CatBoost and SHAP Analysis

This repository contains the source code and materials for the paper "Interpretable Prediction of Geopolymer Concrete Compressive Strength Using DBO-CatBoost and SHAP Analysis" (Currently under review).

## Overview
The construction sector is under a critical need to minimize its carbon footprint, which is now stimulating the development of geopolymer concrete, using recycled coarse aggregates as an eco-friendly material in comparison with Portland cement. Accurate prediction of the compressive strength of this eco-efficient concrete is complex, however, as a result of the complex, nonlinear interactions between many of the mix-design and curing parameters. Although modern scientific literature and engineering practices have increasingly adopted machine learning (ML) for concrete strength prediction, a significant scientific gap remains. Most existing studies rely on “black-box” models that lack sufficient interpretability and frequently overlook the severe risk of data leakage during validation, limiting their practical engineering application. To address this gap, this study proposes a robust, data-leakage-aware framework driven by a rigorous nested GroupKFold cross-validation strategy. By grouping concrete samples by their unique Mix_ID, this approach ensures genuine generalization to entirely unseen mixtures. Within this reliable validation scheme, the CatBoost algorithm is utilized for compressive strength prediction, with the Dung Beetle Optimizer (DBO) serving as an effective tool for hyperparameter tuning. The evaluation results show that the DBO-CatBoost model significantly outperforms the baseline model (CatBoost), Support Vector Regression (SVR), and the Random Forest model with the most stable distribution of the errors, excellent predictive accuracy (R^2=0.9996, RMSE=0.3411, MAPE=0.5699%), and the best accuracy. In addition, the model predictions were demystified using the method of SHapley Additive exPlanations (SHAP) and Partial Dependence Plots (PDP). The interpretability analysis showed that Curing Time and Coarse Aggregate are the most prominent individual predictors and the strongest pairwise interaction between each other; the NaOH molar concentration is the most important second-level influence on optimization of strength. Overall, the framework provides a robust data-driven screening tool that can assist in preliminary mix design evaluation. By reducing the reliance on extensive empirical 'trial and error' approaches, this predictive model supports more efficient material usage and facilitates preliminary optimization of low-carbon concrete formulations.
 Theoretically, this study advances the fundamental science of geopolymer materials by explicitly quantifying the complex, non-linear interactions between alkaline activators, curing conditions, and recycled aggregates. This provides a robust data-driven theoretical foundation for designing and optimizing next-generation eco-friendly concrete products and structures.

## Repository Structure
- `DBO_CatBoost_SHAP_Analysis.ipynb`: The main Jupyter Notebook containing data preprocessing, model training (DBO-CatBoost), and SHAP analysis.
- `requirements.txt`: List of dependencies required to run the code.
- `Data/`: Directory containing the dataset (or sample dataset).

## Installation
To run the code, you need Python 3.x. Install the required packages using:
```bash
pip install -r requirements.txt

## Usage
Open the Jupyter Notebook and run the cells sequentially to reproduce the results and SHAP visualizations.


