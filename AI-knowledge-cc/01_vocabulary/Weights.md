# Weights

## Definition (English)
Weights are the learnable parameters of a neural network that determine the strength of the connection between two neurons. Each input to a neuron is multiplied by its corresponding weight before being summed. During training, weights are iteratively adjusted via backpropagation and gradient descent to minimize the loss function. The final values of the weights encode everything the network has learned.

## Chinese
权重

## German
die Gewichte (die Gewichtungen)

## Intuition
Think of weights as the "importance dials" for each input. When deciding whether to approve a loan, a bank considers income, credit score, and debt. But income might be 3× more important than debt — that's a weight of 3 vs. 1. Before training, weights are random (the network knows nothing). After training on thousands of loan examples, the weights encode the optimal importance of each factor. The learned weights ARE the model.

## Example
A simple neuron: `output = ReLU(w1*income + w2*credit_score + w3*debt + bias)`. Initially w1, w2, w3 are random small numbers. After training: w1=2.3 (income is highly predictive), w2=1.8 (credit score matters), w3=-0.9 (more debt reduces approval chance — negative weight). The bias shifts the decision threshold.

## Spoken Version
"Weights are what the network actually learns — they're the 'knowledge' of the model. Good weights produce good predictions. Backpropagation tells us how to adjust them; gradient descent does the adjusting."

## German Workplace Example
"Die Gewichte sind das, was das Netzwerk tatsächlich lernt — sie sind das 'Wissen' des Modells. Gute Gewichte führen zu guten Vorhersagen."

## Related Concepts
- [[Neuron]]
- [[Backpropagation]]
- [[Gradient Descent]]
- [[Activation Function]]
- [[Neural Networks]]
- [[Training Set]]

## Tags
#neural-networks #weights #parameters #deep-learning
