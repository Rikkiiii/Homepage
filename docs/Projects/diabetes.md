# Bayesian Analysis of Diabetes Predictors

## 📌 Abstract
This study applied a **Bayesian statistical approach** to analyze predictors of diabetes prevalence using the **Pima Indian Diabetes Database**.  
Key predictors identified were **Glucose, BMI, and Diabetes Pedigree Function**, with age also playing an important role when informative priors were introduced.

---

## 🎯 Objectives
- Identify significant predictors of diabetes.  
- Evaluate the effect of **different prior distributions** on posterior estimates.  
- Compare Bayesian methods with traditional frequentist approaches in terms of accuracy, interpretability, and robustness.

---

## 🧪 Methodology
- **Dataset**: 768 patients (female, Pima Indian descent, age ≥ 21).  
- **Data Cleaning**: Removed implausible zero values for BMI, Blood Pressure, etc. (final dataset: 392 records).  
- **Statistical Method**:  
  - Logistic regression with 8 predictors.  
  - Bayesian estimation using **PROC MCMC in SAS** with 100,000 MCMC iterations.  
  - Both non-informative and informative priors tested (e.g., age given prior mean = 0.3).  

- **Diagnostics**:  
  - Checked **trace plots, density plots, MCSE, and ESS** for convergence.  
  - Performed **posterior predictive checks**.  

---

## 📊 Results
- **Significant Predictors**: Glucose, BMI, and Diabetes Pedigree Function.  
- **Age Effect**: More evident with informative prior; higher age → higher diabetes risk.  
- **Model Accuracy**:  
  - Accuracy: 57.14%  
  - Sensitivity: 27.52% (low, many cases missed)  
  - Specificity: 65.62% (better at identifying non-diabetics)  

- **Visualization**:  
  - Histograms of posterior probabilities showed increasing diabetes risk with age.  
  - Informative priors improved convergence and interpretability.

---

## 💡 Discussion
- Bayesian methods provided **better interpretability** and allowed integration of prior knowledge.  
- Imbalanced dataset (67% non-diabetics vs 33% diabetics) biased predictions; resampling and Bayesian bootstrapping could improve results.  
- Suggested improvements:  
  - Apply **Generalized Additive Models (GAM)** for non-linear effects.  
  - Use **weighted priors** or rebalancing for skewed class distribution.  

---

## 🛠 Tools
- **Software**: SAS (PROC MCMC, PROC GAM, PROC LOGISTIC)  
- **Techniques**: Bayesian logistic regression, MCMC diagnostics, posterior predictive checks  

---

## 📖 References
- van de Schoot et al. (2014). *A Gentle Introduction to Bayesian Analysis.* Child Development.  
- Gelman et al. (2004). *Bayesian Data Analysis.*  
- Zou et al. (2017). *Risk Factors of Type 2 Diabetes in China.*  
