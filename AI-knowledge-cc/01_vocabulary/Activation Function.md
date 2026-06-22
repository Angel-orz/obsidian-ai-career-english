# Activation Function

## Definition (English)
An activation function is a non-linear mathematical function applied to the output of a neuron. It determines whether and how strongly the neuron's signal should propagate to the next layer. Without activation functions, a neural network — no matter how deep — would be equivalent to a single linear transformation, incapable of learning complex patterns.

## Chinese
激活函数

## German
die Aktivierungsfunktion

## Intuition
Imagine a bouncer at a club. The bouncer checks each person (input signal) and decides: let them in as-is (linear), only let them in if they meet a minimum standard (ReLU), or map their "loudness" to a 0-1 probability (sigmoid). Different activation functions are like different bouncer policies — ReLU is the popular one that only lets positive energy through; sigmoid squashes everyone into a probability between 0 and 1.

## Example
Common activation functions:
- **ReLU(x) = max(0, x)** — "If the signal is positive, pass it; otherwise, zero." Default for hidden layers in modern networks.
- **Sigmoid(x) = 1/(1+e^(-x))** — Squashes any input into (0, 1), useful for binary classification output.
- **Softmax** — Converts a vector into a probability distribution, used for multi-class output layers.
- **Tanh(x)** — Squashes into (-1, 1), zero-centered, used in RNNs.

## Spoken Version
"Activation functions are what give neural networks their power — without non-linearity, stacking 100 layers is mathematically identical to one layer. ReLU is the default for hidden layers; sigmoid or softmax for output layers depending on the task."

## German Workplace Example
"Aktivierungsfunktionen geben neuronalen Netzen ihre Leistungsfähigkeit. Ohne Nichtlinearität wären 100 gestapelte Schichten mathematisch identisch mit einer einzigen Schicht."

## Related Concepts
- [[Neuron]]
- [[Hidden Layer]]
- [[Backpropagation]]
- [[Neural Networks]]
- [[Vanishing Gradient]]

## Tags
#neural-networks #activation-function #deep-learning
