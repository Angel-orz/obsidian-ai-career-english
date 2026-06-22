# Neural Networks

## Definition (English)
A Neural Network is a computational model inspired by the human brain, consisting of interconnected layers of neurons that learn to map inputs to outputs from data. Each neuron computes a weighted sum of its inputs, applies a non-linear activation function, and passes the result forward. Networks learn by adjusting weights via backpropagation and gradient descent to minimize a loss function. "Deep" neural networks have multiple hidden layers, enabling them to learn hierarchical representations — from simple edges to complex objects.

## Chinese Explanation
神经网络是一种受人脑启发的计算模型，由相互连接的神经元层组成，从数据中学习从输入到输出的映射。每个神经元计算其输入的加权和，应用非线性激活函数，并将结果向前传递。网络通过反向传播和梯度下降调整权重来最小化损失函数。"深度"神经网络有多个隐藏层，能够学习层次化的表示——从简单边缘到复杂物体。

## German Explanation
Ein neuronales Netzwerk ist ein vom menschlichen Gehirn inspiriertes Rechenmodell, das aus miteinander verbundenen Schichten von Neuronen besteht, die lernen, Eingaben aus Daten auf Ausgaben abzubilden. Jedes Neuron berechnet eine gewichtete Summe seiner Eingaben, wendet eine nichtlineare Aktivierungsfunktion an und gibt das Ergebnis weiter. Netzwerke lernen durch Anpassung der Gewichte mittels Backpropagation und Gradientenabstieg, um eine Verlustfunktion zu minimieren.

## Intuition
Neural networks are like a factory assembly line where each station (layer) transforms the product a little more:
1. **Input layer**: Raw materials come in (pixels, text, numbers)
2. **Hidden layers**: Each station refines the product — rough shape → detailed contours → polished finish
3. **Output layer**: Final inspection — "this is a cat" or "this house is worth €450,000"

The beauty is that no one programs the stations. The network discovers the best transformations by looking at thousands of examples and adjusting its weights. A neuron doesn't "know" it's detecting an edge — it just found that certain pixel patterns help reduce the prediction error.

## How It Works

### Architecture
- **Input Layer**: One neuron per feature (e.g., 784 neurons for 28×28 images)
- **Hidden Layers**: Variable number of neurons per layer. More neurons = more capacity to learn, but more risk of overfitting
- **Output Layer**: For classification, one neuron per class with softmax; for regression, one neuron with linear activation

### Training Process
1. **Initialize**: Random small weights
2. **Forward Pass**: Input → Hidden Layer 1 → Hidden Layer 2 → ... → Output → Loss
3. **Backward Pass (Backpropagation)**: Compute gradient of loss w.r.t. every weight using chain rule
4. **Update**: w = w - learning_rate × gradient (Gradient Descent)
5. **Repeat**: Thousands of iterations until convergence

### Key Design Choices
- **Width vs Depth**: Wide shallow networks memorize; deep narrow networks generalize better
- **Activation Functions**: ReLU for hidden layers (fast, avoids vanishing gradient); sigmoid/softmax for output
- **Regularization**: Dropout, weight decay, early stopping to prevent overfitting

## Real-world Examples
1. **Image Classification** — ResNet-50 classifies 1.2M ImageNet images into 1000 categories with 76% top-1 accuracy
2. **Speech Recognition** — Deep neural networks power Siri, Alexa, and Google Assistant's ability to transcribe speech to text
3. **Recommendation Systems** — YouTube's neural network recommends videos by learning embeddings for users and content

## Interview Answer

> "A neural network is a stack of layers where each layer applies a linear transformation followed by a non-linear activation. What makes them powerful is that, given enough neurons and layers, they can approximate any continuous function — this is the Universal Approximation Theorem.
>
> Training works via backpropagation: we do a forward pass to compute predictions and loss, then apply the chain rule backward to compute the gradient of the loss with respect to every weight. Gradient descent then updates each weight to reduce the loss. This repeats for many epochs.
>
> The key practical considerations are: choosing the right architecture (how many layers, how many neurons per layer), picking appropriate activation functions (ReLU for hidden layers is the safe default), preventing overfitting with dropout or weight decay, and tuning the learning rate — too high and training diverges, too low and it takes forever.
>
> Modern frameworks like PyTorch and TensorFlow handle the backpropagation automatically via autograd — you just define the forward pass. But understanding the math underneath is critical for debugging when training doesn't converge."

## Related Concepts
- [[Neuron]]
- [[Activation Function]]
- [[Hidden Layer]]
- [[Backpropagation]]
- [[Weights]]
- [[Gradient Descent]]
- [[Loss Function]]
- [[Overfitting]]
- [[Convolutional Neural Network]]
- [[Transformer]]
