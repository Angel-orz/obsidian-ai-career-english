---
topic: Classification & Regression
date: 2026-06-19
---

# Interview — Classification & Regression

## Question

> **"Explain the difference between classification and regression. When would you use one over the other? Give concrete examples from your experience."**

This is a fundamental ML interview question asked at nearly every company — from Bosch and Siemens to Amazon and Google. Interviewers use it to verify you understand the basics before moving to advanced topics.

## 30-Second Answer

"Classification predicts a category — like whether an email is spam or not. Regression predicts a continuous number — like a house price. The rule of thumb: 'which one?' → classification, 'how much?' → regression. The choice affects which algorithms, loss functions, and evaluation metrics you use. A typical classification project might use logistic regression with F1-score, while a regression project might use gradient boosting with RMSE."

## Strong Answer

"The distinction is fundamental. Classification outputs a discrete class label from a finite set — binary like fraud/legitimate, or multi-class like classifying images into 1,000 categories. Regression outputs a continuous value — any real number, like predicting temperature or revenue.

This choice cascades through the entire ML pipeline:

First, **algorithm selection**: For classification, I'd start with logistic regression as an interpretable baseline, then explore tree-based methods or neural networks with softmax. For regression, linear regression is the natural baseline, with gradient boosting or neural networks for non-linear relationships.

Second, **loss function**: Classification typically uses cross-entropy loss, which heavily penalizes confident wrong predictions. Regression uses MSE or MAE — MSE penalizes large errors more heavily due to squaring, while MAE is more robust to outliers.

Third, **evaluation**: Accuracy is the most intuitive classification metric, but it fails on imbalanced data. I'd use precision, recall, F1-score, and ROC-AUC, always examining the confusion matrix. For regression, RMSE tells me the typical error magnitude in the original units, while R² tells me how much variance the model explains.

Fourth, **output interpretation**: Classification gives probabilities I can threshold — in fraud detection, I might set a low threshold to catch more fraud at the cost of more false alarms. Regression gives a point estimate, and I'd often add prediction intervals to quantify uncertainty.

Real examples from my work: when building a customer churn predictor, I used binary classification with logistic regression and optimized for recall — missing a churner costs more than offering an unnecessary discount. When estimating used car prices for a marketplace, I used gradient boosting regression with MAE — stakeholders wanted the average error in euros, not squared euros.

A common pitfall: treating an ordinal problem as pure classification when regression preserves the ordering. Customer satisfaction on a 1-5 scale — regression captures that 4 is closer to 5 than to 1; one-hot classification loses that structure."

## Common Mistakes

1. **Using accuracy on imbalanced data**
   - ❌ "The model has 99% accuracy" when only 1% of cases are positive
   - ✅ Use precision, recall, F1, or AUC-ROC for imbalanced datasets

2. **Confusing logistic regression with regression**
   - ❌ "Logistic regression is for regression because it's in the name"
   - ✅ Logistic regression outputs probabilities for classification — the name is historical

3. **Applying regression to ordinal data without consideration**
   - ❌ Treating movie ratings (1-5 stars) as independent classes
   - ✅ Consider ordinal regression or treat as regression to preserve ordering, depending on the use case

4. **Choosing RMSE without checking for outliers**
   - ❌ "RMSE is the standard, I always use it"
   - ✅ Check for outliers first — RMSE squares errors, so outliers dominate. MAE or Huber loss may be better

5. **Not asking the business question before choosing**
   - ❌ Jumping straight to "I'll use a random forest classifier"
   - ✅ First ask: "What decision will be made with this prediction? What's the cost of different errors?"

## Related
- [[Classification & Regression]] (02_concepts)
- [[Classification & Regression]] (03_speaking)
