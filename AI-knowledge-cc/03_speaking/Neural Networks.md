---
topic: Neural Networks
date: 2026-06-20
---

# Speaking — Neural Networks

## 30-Second Version
"A neural network is a stack of layers of neurons that learn patterns from data. Each neuron takes inputs, weights them by importance, and passes the result through an activation function. The network learns by making predictions, measuring errors, and adjusting every weight backward through the network — that's backpropagation. With enough layers, neural networks can learn incredibly complex patterns, which is why they power everything from face recognition to ChatGPT."

## 60-Second Version
"Neural networks are the foundation of modern deep learning. The core idea is simple but powerful: stack layers of neurons, where each neuron computes a weighted sum of its inputs and applies a non-linear activation like ReLU.

The learning process has two phases. In the forward pass, data flows from input to output, and we compute the loss — how wrong the prediction is. In the backward pass, we use backpropagation — essentially the chain rule from calculus — to compute how much each weight contributed to that error. Then gradient descent nudges every weight to reduce the loss.

What makes deep networks special is that each hidden layer learns progressively more abstract features. In an image network, layer 1 detects edges, layer 2 detects shapes, layer 3 detects objects. No one programmed these features — the network discovered them from data.

The key practical challenges: choosing the architecture, preventing overfitting with dropout or weight decay, and tuning the learning rate. Too high and training diverges; too low and it takes forever."

## Keywords List
| English | Chinese | German |
|---------|---------|--------|
| Neuron | 神经元 | das Neuron |
| Activation Function | 激活函数 | die Aktivierungsfunktion |
| Hidden Layer | 隐藏层 | die versteckte Schicht |
| Backpropagation | 反向传播 | die Backpropagation |
| Weights | 权重 | die Gewichte |
| Gradient Descent | 梯度下降 | der Gradientenabstieg |
| Forward Pass | 前向传播 | der Vorwärtsdurchlauf |
| Loss Function | 损失函数 | die Verlustfunktion |
| Epoch | 训练轮次 | die Epoche |
| Overfitting | 过拟合 | die Überanpassung |

## German Summary
Neuronale Netzwerke bestehen aus gestapelten Schichten von Neuronen, die Muster aus Daten lernen. Jedes Neuron berechnet eine gewichtete Summe und wendet eine Aktivierungsfunktion an. Das Netzwerk lernt durch Backpropagation — die Fehler werden rückwärts durch das Netz propagiert, und jeder Gewicht wird angepasst, um den Fehler zu reduzieren.

## Related
- [[Neural Networks]] (02_concepts)
- [[Neural Networks]] (04_meetings)
- [[Neural Networks]] (05_interview)
