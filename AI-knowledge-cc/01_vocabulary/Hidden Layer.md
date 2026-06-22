# Hidden Layer

## Definition (English)
A hidden layer is any layer of neurons between the input layer and the output layer in a neural network. Each hidden layer transforms its input into a progressively more abstract representation. "Deep" learning refers to networks with multiple hidden layers. The first hidden layer might detect edges, the second shapes, the third objects — each layer builds on the previous one's output.

## Chinese
隐藏层

## German
die versteckte Schicht (der Hidden Layer)

## Intuition
Think of an assembly line in a factory. The raw materials (input data) pass through multiple stations (hidden layers). Station 1 rough-cuts the material, Station 2 refines the shape, Station 3 adds detail, and the final station packages the finished product (output). No single station does everything — each specializes in one transformation. The "hidden" part just means you don't directly observe these intermediate representations during training.

## Example
In a face recognition network:
- **Hidden Layer 1**: Detects edges and simple textures from raw pixels
- **Hidden Layer 2**: Combines edges into shapes — eyes, noses, mouths
- **Hidden Layer 3**: Combines shapes into face parts
- **Hidden Layer 4**: Represents complete face identity

Each hidden layer's output is called an "embedding" or "representation" — a compressed, meaningful encoding of the input.

## Spoken Version
"Hidden layers are where the learning actually happens — each layer extracts features at a different level of abstraction. The more hidden layers, the more hierarchical and abstract the features your network can learn."

## German Workplace Example
"Versteckte Schichten sind der Ort, an dem das eigentliche Lernen stattfindet. Jede Schicht extrahiert Merkmale auf einer anderen Abstraktionsebene — je mehr Schichten, desto hierarchischer die gelernten Repräsentationen."

## Related Concepts
- [[Neuron]]
- [[Activation Function]]
- [[Backpropagation]]
- [[Neural Networks]]
- [[Deep Learning]]

## Tags
#neural-networks #hidden-layer #deep-learning
