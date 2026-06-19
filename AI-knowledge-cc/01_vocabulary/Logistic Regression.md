# Logistic Regression

## Definition (English)
Logistic Regression is a classification algorithm that predicts the probability that an input belongs to a particular class. Despite its name, it is used for classification, not regression. It applies the sigmoid function to a linear combination of input features, squashing the output into a range between 0 and 1, which can be interpreted as a probability. A threshold (typically 0.5) converts the probability into a class label.

## Chinese
逻辑回归

## German
die logistische Regression

## Intuition
A linear regression might predict any number from negative infinity to positive infinity — useless for a yes/no question. Logistic regression takes that raw number and runs it through an S-shaped sigmoid curve that compresses it between 0 and 1. Values above 0 map to probabilities above 50%, and values below 0 map to probabilities below 50%. It's the simplest neural network: one layer with a sigmoid activation.

## Example
A bank uses logistic regression to predict whether a loan applicant will default. Input features: income, credit score, debt-to-income ratio. The model outputs 0.73 → 73% probability of default. Since 0.73 > 0.5, the model classifies this applicant as "will default." The bank can adjust the threshold to be more conservative (e.g., 0.3) if missing defaults is very costly.

## Spoken Version
"Logistic regression is the go-to baseline for binary classification — it's simple, interpretable, and outputs calibrated probabilities via the sigmoid function. Despite the name, it's a classification algorithm."

## German Workplace Example
"Die logistische Regression ist die erste Wahl als Baseline für binäre Klassifikation. Sie ist einfach, interpretierbar und gibt kalibrierte Wahrscheinlichkeiten über die Sigmoid-Funktion aus. Trotz des Namens ist sie ein Klassifikationsalgorithmus."

## Related Concepts
- [[Classification]]
- [[Regression]]
- [[Decision Boundary]]
- [[Sigmoid Function]]
- [[Linear Regression]]
- [[Confusion Matrix]]

## Tags
#classification #logistic-regression #algorithms #ml-fundamentals
