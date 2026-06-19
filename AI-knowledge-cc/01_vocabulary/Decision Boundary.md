# Decision Boundary

## Definition (English)
A decision boundary is the surface (line, curve, or hyperplane) that separates different classes in a classification model. On one side of the boundary, the model predicts Class A; on the other side, Class B. For binary classification, it's the line where the model transitions from predicting one class to the other.

## Chinese
决策边界

## German
die Entscheidungsgrenze

## Intuition
Imagine drawing a line on a map separating two countries. Everything north of the line is Germany, everything south is Austria. A decision boundary works the same way: it's the "border" the model draws through the feature space to separate categories. Linear models draw straight lines; neural networks can draw highly complex, curved boundaries.

## Example
For a spam classifier using two features — number of exclamation marks and presence of the word "free" — the decision boundary might be a line where emails above it are classified as spam and below it as not spam. A logistic regression model learns the optimal position and angle of this line from training data.

## Spoken Version
"The decision boundary is where the model switches its prediction from one class to another — linear models produce straight boundaries, while deep networks can learn arbitrarily complex shapes."

## German Workplace Example
"Die Entscheidungsgrenze ist der Punkt, an dem das Modell seine Vorhersage von einer Klasse zur anderen wechselt. Lineare Modelle erzeugen gerade Grenzen, während tiefe Netzwerke beliebig komplexe Formen lernen können."

## Related Concepts
- [[Classification]]
- [[Logistic Regression]]
- [[Support Vector Machine]]
- [[Overfitting]]
- [[Feature]]

## Tags
#classification #decision-boundary #ml-fundamentals
