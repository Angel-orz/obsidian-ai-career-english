---
tags: [daily-notes]
topic: Neural Networks
date: 2026-06-20
---

# Daily Notes — Neural Networks

## Vocabulary Learned
- [ ] [[Neuron]]
- [ ] [[Activation Function]]
- [ ] [[Hidden Layer]]
- [ ] [[Backpropagation]]
- [ ] [[Weights]]

## Concepts Learned
| Concept | Understanding (1-5) | Notes |
|---------|---------------------|-------|
| Neuron as basic unit | 4 | Weighted sum + activation = neuron output |
| Activation functions | 4 | ReLU default for hidden; sigmoid/softmax for output |
| Hidden layers & hierarchy | 4 | Each layer learns more abstract features |
| Backpropagation | 3 | Chain rule applied backward; need to work through math manually |
| Weight update with gradient descent | 4 | w = w - lr * gradient; learning rate is critical |

## Listening Practice
| Source | Topic | Duration | Key Takeaways |
|--------|-------|----------|---------------|

## Speaking Practice
| Exercise | Completed | Self-Rating |
|----------|-----------|-------------|
| 30-second neural network explanation | [ ] | — |
| 60-second forward/backward pass explanation | [ ] | — |

## Difficulties
- Backpropagation math: need to work through a small example with 2-3 neurons manually to really internalize the chain rule
- Intuition for when to go wider vs deeper — rule of thumb?

## Reflection
- The neuron model is surprisingly simple: weighted sum + activation. The power is entirely in the stacking and the learning algorithm.
- Backpropagation is "just" the chain rule, but understanding it at the implementation level is different from understanding it conceptually.

## Next Steps
- [ ] Work through backpropagation by hand for a tiny 2-layer network
- [ ] Review vocabulary (spaced repetition)
- [ ] Preview next topic: CNN
