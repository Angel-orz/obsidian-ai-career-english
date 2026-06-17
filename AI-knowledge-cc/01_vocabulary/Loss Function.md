# Loss Function

## Definition (English)
A loss function (or cost function) measures how far the model's predictions are from the true labels. It quantifies the "error" — the model's goal during training is to minimize this loss.

## Chinese
损失函数

## German
Verlustfunktion (die Loss Function)

## Intuition
Imagine throwing darts at a target. The loss function measures the distance from each dart to the bullseye. A good model has darts clustered near the center (low loss). Training is the process of adjusting your throw (model parameters) to reduce the average distance.

## Example
In linear regression predicting house prices, Mean Squared Error (MSE) is a common loss function. If the model predicts €300,000 but the actual price is €320,000, the squared error is (320,000 - 300,000)² = 400 million. The model adjusts to make this number smaller over time.

## Spoken Version
"We're using cross-entropy loss for this classification task — it penalizes confident wrong predictions more heavily, which helps the model converge faster."

## German Workplace Example
"Für diese Klassifikationsaufgabe verwenden wir Cross-Entropy-Loss. Diese Verlustfunktion bestraft selbstbewusste Fehlvorhersagen stärker, was dem Modell hilft, schneller zu konvergieren."

## Related Concepts
- [[Gradient Descent]]
- [[Optimization]]
- [[Mean Squared Error]]
- [[Cross-Entropy]]

## Tags
#supervised-learning #loss-function #optimization #training
