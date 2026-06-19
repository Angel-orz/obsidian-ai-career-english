# Classification & Regression

## Definition (English)
Classification and Regression are the two main types of supervised learning tasks. **Classification** predicts a discrete category label (e.g., spam/not spam, disease diagnosis). **Regression** predicts a continuous numerical value (e.g., house price, temperature, stock return). Both learn a mapping function `f(x) = y` from labeled training data, but they differ in the type of `y` they produce — categorical vs. continuous — which determines the choice of algorithm, loss function, and evaluation metrics.

## Chinese Explanation
分类和回归是监督学习的两种主要类型。分类预测离散的类别标签（如垃圾邮件/非垃圾邮件、疾病诊断），而回归预测连续的数值（如房价、温度、股票回报率）。两者都从带标签的训练数据中学习映射函数 f(x) = y，但它们产生的 y 类型不同——类别型 vs. 连续型——这决定了算法、损失函数和评估指标的选择。

## German Explanation
Klassifikation und Regression sind die beiden Hauptarten des überwachten Lernens. Bei der Klassifikation wird eine diskrete Kategorie vorhergesagt (z. B. Spam/kein Spam, Krankheitsdiagnose), bei der Regression ein kontinuierlicher numerischer Wert (z. B. Immobilienpreis, Temperatur, Aktienrendite). Beide lernen eine Abbildungsfunktion f(x) = y aus beschrifteten Trainingsdaten, unterscheiden sich jedoch in der Art des vorhergesagten y — kategorial vs. kontinuierlich — was die Wahl des Algorithmus, der Verlustfunktion und der Evaluierungsmetriken bestimmt.

## Intuition
Think of a teacher grading two types of assignments:
- **Classification** = Multiple-choice questions. The answer is one of A, B, C, or D. You're either right or wrong. There's no "almost C."
- **Regression** = Essay scoring on a 0–100 scale. The answer is a number along a spectrum. A prediction of 78 when the true score is 82 is "close but not exact."

The practical rule: if you find yourself asking "which one?" → classification. If you find yourself asking "how much?" → regression. A spam filter asks "which one?" (spam or not). A house price predictor asks "how much?" (in euros).

Some problems can be framed either way. Predicting student performance could be regression (predict exact score: 87.3) or classification (predict letter grade: A, B, C, D, F). The choice depends on what decision you'll make with the prediction.

## How It Works

### Classification Workflow
1. **Define classes** — Binary (2 classes) or multi-class (3+ classes)
2. **Choose algorithm** — Logistic Regression, Decision Trees, Random Forest, SVM, Neural Networks
3. **Train** — Model learns decision boundaries that separate classes in feature space
4. **Predict** — Output a class label (hard classification) or probability per class (soft classification)
5. **Evaluate** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix, ROC-AUC

### Regression Workflow
1. **Define target** — Continuous variable to predict
2. **Choose algorithm** — Linear Regression, Polynomial Regression, Random Forest Regressor, Gradient Boosting, Neural Networks
3. **Train** — Model learns the function that best fits the data by minimizing prediction error
4. **Predict** — Output a continuous number
5. **Evaluate** — MAE (Mean Absolute Error), MSE (Mean Squared Error), RMSE, R² Score

### Key Differences

| Aspect | Classification | Regression |
|--------|---------------|------------|
| Output Type | Discrete class | Continuous number |
| Question Answered | "Which category?" | "How much?" |
| Loss Function | Cross-Entropy, Hinge Loss | MSE, MAE, Huber Loss |
| Evaluation | Accuracy, F1, Confusion Matrix | RMSE, R², MAE |
| Decision Surface | Decision boundaries | Regression line/surface |
| Example | Spam detection | House price prediction |

## Real-world Examples

### Classification
1. **Email Spam Detection** — Binary classification: ham (0) or spam (1). Gmail processes 300+ billion emails daily with >99.9% accuracy.
2. **Medical Image Diagnosis** — Multi-class: "normal," "benign tumor," "malignant tumor." Models like CheXNet match radiologist performance on chest X-rays.
3. **Customer Churn Prediction** — Binary: will churn (1) or won't churn (0). Telecom companies use this to target retention offers.

### Regression
1. **Real Estate Valuation** — Predict continuous sale price. Zillow's Zestimate uses regression over hundreds of features (location, sqft, bedrooms, school ratings).
2. **Energy Load Forecasting** — Predict electricity demand in megawatts for the next 24 hours. Grid operators use this to balance supply and demand.
3. **Used Car Pricing** — mobile.de and AutoScout24 estimate market value from mileage, age, brand, and condition.

### Hybrid Cases
- **Weather forecasting**: Temperature prediction is regression; rain/no-rain is classification.
- **Autonomous driving**: Steering angle is regression; traffic sign recognition is classification.

## Interview Answer

> "Classification and regression are the two fundamental types of supervised learning, and the distinction is simple: classification predicts a category, regression predicts a number.
>
> In classification, the model learns decision boundaries that separate classes. For binary classification — spam vs. not spam, fraud vs. legitimate — we use algorithms like logistic regression, decision trees, or SVMs. For multi-class problems like image recognition with 1,000 categories, we typically use neural networks with softmax outputs. We evaluate with accuracy, precision, recall, F1-score, and confusion matrices — accuracy alone can be misleading when classes are imbalanced.
>
> In regression, the model learns a continuous function from inputs to outputs. House price prediction, demand forecasting, and temperature estimation are all regression problems. We use linear regression as a baseline, but tree-based methods like gradient boosting often outperform for tabular data. Evaluation uses error metrics — MAE, MSE, RMSE — which tell you how far off your predictions are in the original units.
>
> The choice between them drives every downstream decision: which algorithms are appropriate, which loss function to optimize, what 'good performance' means, and how to communicate results to stakeholders. A common trap is treating an ordinal problem as classification when regression would capture more nuance — for example, predicting customer satisfaction on a 1-5 scale: regression preserves the ordering; classification treats each rating as independent."

## Related Concepts
- [[Supervised Learning]]
- [[Unsupervised Learning]]
- [[Classification]]
- [[Regression]]
- [[Logistic Regression]]
- [[Confusion Matrix]]
- [[Decision Boundary]]
- [[Loss Function]]
- [[Overfitting]]
- [[Labeled Data]]
- [[Feature]]
- [[Training Set]]
