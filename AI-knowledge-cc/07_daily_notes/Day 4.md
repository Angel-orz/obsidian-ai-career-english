I built a complete machine learning pipeline using scikit-learn.
我用 scikit-learn 搭建了一个完整的机器学习流水线。

I compared three models: logistic regression, random forest, and SVM.
我对比了三个模型：逻辑回归、随机森林和支持向量机。

The pipeline includes data preprocessing, feature engineering,
and model evaluation.
这个流水线包括数据预处理、特征工程和模型评估。

I used five-fold cross-validation to get a more robust
performance estimate.
我使用了五折交叉验证来获得更稳健的性能评估。

Random forest achieved the best ROC-AUC score of zero point eight five.
随机森林取得了 0.85 的最佳 ROC-AUC 分数。

I always split the data before any preprocessing to prevent data leakage.

For imbalanced datasets, accuracy is misleading. I always check precision, recall, and ROC-AUC together to understand the full picture.

面试问题： "How do you evaluate a classification model?"

▎ ① "I look at multiple metrics, not just accuracy — especially for imbalanced datasets."
▎
▎ ② "Precision and recall tell me about false positive vs false negative tradeoffs. ROC-AUC gives an overall picture of the model's ability to separate classes."
▎
▎ ③ "I always use stratified k-fold cross-validation to ensure the evaluation is robust and not dependent on a single lucky split. I also check the confusion matrix to understand the exact error patterns."