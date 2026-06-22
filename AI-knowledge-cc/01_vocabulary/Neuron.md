# Neuron

## Definition (English)
A neuron (or node) is the basic computational unit of a neural network. It receives multiple inputs, computes a weighted sum, adds a bias term, and passes the result through an activation function to produce an output. A single neuron performs a simple operation, but thousands or millions of neurons connected in layers can approximate extremely complex functions.

## Chinese
神经元

## German
das Neuron (der Knoten)

## Intuition
Think of a neuron as a tiny decision-maker. It looks at several pieces of evidence (inputs), weights how important each piece is (weights), and makes a simple yes/no-or-something-in-between call (activation). One neuron might detect "is there an edge in this part of the image?" — too simple to recognize a face. But stack thousands of these tiny decisions together, and the network can recognize your grandmother.

## Example
A neuron in the first hidden layer of an image classifier takes pixel values as inputs. It computes: `output = ReLU(w1*pixel1 + w2*pixel2 + ... + wn*pixeln + bias)`. If the weighted sum crosses a threshold, the neuron "fires" and passes a signal forward. The activation function (ReLU) keeps only positive signals, adding non-linearity.

## Spoken Version
"A neuron is just a weighted sum followed by a non-linear activation. The magic isn't in a single neuron — it's in stacking millions of them into deep networks, where each layer learns progressively more abstract features."

## German Workplace Example
"Ein Neuron ist im Grunde nur eine gewichtete Summe mit einer nichtlinearen Aktivierung. Die eigentliche Stärke liegt nicht in einem einzelnen Neuron, sondern darin, Millionen davon zu tiefen Netzwerken zu stapeln."

## Related Concepts
- [[Activation Function]]
- [[Hidden Layer]]
- [[Backpropagation]]
- [[Weights]]
- [[Neural Networks]]

## Tags
#neural-networks #deep-learning #fundamentals
