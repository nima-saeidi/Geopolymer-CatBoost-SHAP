# Interpretable Prediction of Geopolymer Concrete Compressive Strength Using DBO-CatBoost and SHAP Analysis

[![Paper](https://img.shields.io/badge/Paper-MDPI%20Buildings-blue.svg)](https://www.mdpi.com/2075-5309/16/16/3326)
[![DOI](https://img.shields.io/badge/DOI-10.3390%2Fbuildings16163326-brightgreen.svg)](https://doi.org/10.3390/buildings16163326)

This repository contains the official implementation and source code for the paper:  
**"Interpretable Prediction of Geopolymer Concrete Compressive Strength Using DBO-CatBoost and SHAP Analysis"** published in *MDPI Buildings*.

🔗 **Read the full paper:** [https://www.mdpi.com/2075-5309/16/16/3326](https://www.mdpi.com/2075-5309/16/16/3326)

---

## Overview
The construction sector is under a critical need to minimize its carbon footprint, which is now stimulating the development of geopolymer concrete, using recycled coarse aggregates as an eco-friendly material in comparison with Portland cement. Accurate prediction of the compressive strength of this eco-efficient concrete is complex, however, as a result of the complex, nonlinear interactions between many of the mix-design and curing parameters. Although modern scientific literature and engineering practices have increasingly adopted machine learning (ML) for concrete strength prediction, a significant scientific gap remains. Most existing studies rely on “black-box” models that lack sufficient interpretability and frequently overlook the severe risk of data leakage during validation, limiting their practical engineering application.

To address this gap, this study proposes a robust, data-leakage-aware framework driven by a rigorous nested GroupKFold cross-validation strategy. By grouping concrete samples by their unique `Mix_ID`, this approach ensures genuine generalization to entirely unseen mixtures. Within this reliable validation scheme, the CatBoost algorithm is utilized for compressive strength prediction, with the Dung Beetle Optimizer (DBO) serving as an effective tool for hyperparameter tuning. The evaluation results show that the DBO-CatBoost model significantly outperforms the baseline model (CatBoost), Support Vector Regression (SVR), and the Random Forest model with the most stable distribution of the errors, excellent predictive accuracy ($R^2=0.9996$, $\text{RMSE}=0.3411\text{ MPa}$, $\text{MAPE}=0.5699\%$).

In addition, the model predictions were demystified using SHapley Additive exPlanations (SHAP) and Partial Dependence Plots (PDP). The interpretability analysis showed that **Curing Time** and **Coarse Aggregate** are the most prominent individual predictors with the strongest pairwise interaction; the **NaOH molar concentration** is the most important second-level influence on optimization of strength. Overall, the framework provides a robust data-driven screening tool that can assist in preliminary mix design evaluation, supporting efficient material usage and facilitating the design of low-carbon concrete formulations.

---

## Repository Structure
- `DBO_CatBoost_SHAP_Analysis.ipynb`: The main Jupyter Notebook containing data preprocessing, leakage-free nested GroupKFold cross-validation, hyperparameter tuning with DBO, model evaluation, and SHAP/PDP interpretability analysis.

---

   
