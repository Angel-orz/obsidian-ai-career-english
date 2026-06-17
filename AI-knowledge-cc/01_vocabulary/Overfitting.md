# Overfitting

## Definition (English)
Overfitting happens when a model learns the training data too well — including its noise and random fluctuations — but fails to generalize to new, unseen data. The model "memorizes" rather than "learns."

## Chinese
过拟合

## German
Überanpassung (Overfitting)

## Intuition
Overfitting is like a student who memorizes every practice problem's exact numbers instead of understanding the underlying concept. They get 100% on practice tests but fail the real exam because the questions are slightly different. A good model learns patterns, not specifics.

## Example
A decision tree that keeps splitting until every training data point is perfectly classified — with 100% training accuracy but only 65% test accuracy — is overfitting. It has created rules for noise instead of learning the true decision boundary.

## Spoken Version
"We noticed the training accuracy is 99% but validation is only 72% — clear sign of overfitting. We should add regularization and potentially reduce model complexity."

## German Workplace Example
"Die Trainingsgenauigkeit liegt bei 99%, aber die Validierungsgenauigkeit nur bei 72% — ein klares Anzeichen für Überanpassung. Wir sollten Regularisierung hinzufügen und die Modellkomplexität reduzieren."

## Related Concepts
- [[Underfitting]]
- [[Regularization]]
- [[Generalization]]
- [[Bias-Variance Tradeoff]]

## Tags
#supervised-learning #overfitting #generalization #validation
