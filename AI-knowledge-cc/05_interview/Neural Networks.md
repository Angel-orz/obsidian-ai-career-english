---
topic: Neural Networks
date: 2026-06-20
---

# Interview — Neural Networks

## Question
> "Walk me through how a neural network is trained. What happens in the forward pass and backward pass?"

## 30-Second Answer
"In the forward pass, input data flows through the network layer by layer — each neuron computes a weighted sum and applies an activation function — until we get a prediction and compute the loss. In the backward pass, we use backpropagation, which is the chain rule from calculus, to compute the gradient of the loss with respect to every weight. Then gradient descent updates each weight to reduce the loss. Repeat for many epochs until convergence."

## Strong Answer
"Training a neural network is an iterative optimization process with two phases per iteration.

**Forward Pass:** Input data enters the network. At each layer, every neuron computes `z = Σ(w_i × x_i) + bias`, then applies an activation function like ReLU: `a = max(0, z)`. This output becomes the input to the next layer. This repeats through all hidden layers until the output layer produces a prediction. We then compute the loss — for classification, typically cross-entropy between predicted probabilities and true labels.

**Backward Pass (Backpropagation):** This is where learning happens. We compute the gradient of the loss with respect to every weight in the network, starting from the output layer and working backward using the chain rule. For each weight w, we compute ∂Loss/∂w — how much does a tiny change in w affect the final loss? Frameworks like PyTorch do this automatically via autograd — they build a computation graph during the forward pass and traverse it backward.

**Weight Update:** Using gradient descent, we update each weight: `w_new = w_old — learning_rate × ∂Loss/∂w`. The learning rate is critical — too high and you overshoot the minimum, too low and training takes forever. Modern optimizers like Adam add momentum and adaptive learning rates per parameter.

This entire process repeats for many epochs over the training data, typically in mini-batches for efficiency. We monitor validation loss to detect overfitting and apply early stopping.

The key insight: every weight in the network is updated simultaneously based on its contribution to the error. A network with millions of weights can learn remarkably complex functions this way."

## Common Mistakes
1. **Forgetting non-linearity** — Without activation functions, the entire network collapses to a single linear transformation regardless of depth
2. **Wrong learning rate** — Most common training failure mode; use a learning rate finder or start at 0.001 for Adam
3. **Not normalizing inputs** — Neural networks expect zero-mean, unit-variance inputs; raw data causes slow or failed convergence
4. **Confusing epoch, batch, iteration** — One epoch = one pass through all training data; batch = subset used per update; iteration = one weight update
5. **Ignoring validation loss** — Training loss always decreases; only validation loss tells you if the model is learning vs. memorizing

## Related
- [[Neural Networks]] (02_concepts)
- [[Neural Networks]] (03_speaking)
