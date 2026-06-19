# Confusion Matrix

## Definition (English)
A confusion matrix is a table that visualizes the performance of a classification model by comparing predicted labels against actual labels. For binary classification, it has four cells: True Positives (TP), True Negatives (TN), False Positives (FP), and False Negatives (FN). From these, key metrics like accuracy, precision, recall, and F1-score are calculated.

## Chinese
混淆矩阵

## German
die Konfusionsmatrix (die Wahrheitsmatrix)

## Intuition
Think of a medical test. A confusion matrix tells you four things: (1) sick people correctly diagnosed — TP, (2) healthy people correctly cleared — TN, (3) healthy people wrongly told they're sick — FP, (4) sick people wrongly told they're healthy — FN. The last one is the most dangerous in medicine: a missed diagnosis. The matrix reveals which errors your model makes and at what cost.

## Example
A fraud detection model evaluated on 10,000 transactions:
- TP = 85 (fraud correctly caught)
- TN = 9,800 (legitimate correctly passed)
- FP = 100 (legitimate flagged as fraud — annoying customers)
- FN = 15 (fraud missed — financial loss)

Precision = 85/(85+100) = 45.9%, Recall = 85/(85+15) = 85%. The model catches most fraud (high recall) but annoys some customers (low precision).

## Spoken Version
"Accuracy alone can be misleading — the confusion matrix breaks down performance into true positives, false positives, true negatives, and false negatives, so you can see exactly where your model is failing."

## German Workplace Example
"Die Genauigkeit allein kann irreführend sein. Die Konfusionsmatrix zerlegt die Leistung in richtig-positive, falsch-positive, richtig-negative und falsch-negative Ergebnisse, sodass Sie genau sehen können, wo Ihr Modell versagt."

## Related Concepts
- [[Classification]]
- [[Precision and Recall]]
- [[F1 Score]]
- [[ROC Curve]]
- [[Imbalanced Data]]

## Tags
#classification #evaluation #metrics #ml-fundamentals
