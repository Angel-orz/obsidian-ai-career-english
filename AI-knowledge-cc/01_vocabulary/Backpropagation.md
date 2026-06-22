# Backpropagation

## Definition (English)
Backpropagation (backward propagation of errors) is the algorithm that trains neural networks by computing gradients of the loss function with respect to every weight in the network. It works in two phases: (1) forward pass — compute predictions and loss; (2) backward pass — apply the chain rule from calculus to propagate the error gradient from the output layer back to the input layer, updating each weight to reduce the loss.

## Chinese
反向传播

## German
die Backpropagation (die Fehlerrückführung)

## Intuition
Imagine you're tuning a guitar with many strings. You pluck the final string (output), hear it's off-pitch (loss), and work backward: "The pitch error came from this tuning peg being too tight, which was caused by that bridge being misaligned..." You adjust each part proportional to how much it contributed to the error. Backpropagation does exactly this — it assigns "credit" (or "blame") for the final error to each weight, layer by layer, from output to input.

## Example
Training a simple network on MNIST digit classification:
1. **Forward pass**: Image pixels → hidden layer → output (prediction: "3")
2. **Compute loss**: Cross-entropy between predicted "3" and true label "7"
3. **Backward pass**: Compute ∂Loss/∂w for every weight w using chain rule
4. **Update**: w_new = w_old - learning_rate × ∂Loss/∂w
5. **Repeat** thousands of times until the network correctly classifies digits

## Spoken Version
"Backpropagation is just the chain rule applied to neural networks — it efficiently computes how much each weight contributed to the error, so we can nudge every weight in the right direction. It's the engine behind all modern deep learning."

## German Workplace Example
"Backpropagation ist im Grunde die Kettenregel, angewendet auf neuronale Netze. Sie berechnet effizient, wie stark jedes Gewicht zum Fehler beigetragen hat, sodass wir jedes Gewicht in die richtige Richtung anpassen können."

## Related Concepts
- [[Gradient Descent]]
- [[Loss Function]]
- [[Neuron]]
- [[Weights]]
- [[Neural Networks]]
- [[Vanishing Gradient]]

## Tags
#neural-networks #backpropagation #training #deep-learning
