# Convolution

## Definition (English)
Convolution is a mathematical operation that slides a small matrix (kernel/filter) over an input, computing element-wise multiplications and summing the results at each position. In CNNs, convolution layers learn filter weights to detect visual patterns like edges, textures, and shapes. It preserves spatial structure — unlike fully connected layers which flatten the input.

## Chinese
卷积

## German
die Faltung (die Konvolution)

## Intuition
Imagine moving a magnifying glass over a map. At each position, you only look at the small area under the glass. A convolution does this: a small filter (3x3 pixels) slides across the entire image, and at each stop, computes "how much does this patch match my pattern?" The result is a feature map showing where that pattern was found.

## Example
A 3x3 edge-detection filter slides across a 28x28 MNIST digit image. At each valid position, it multiplies its 9 weights by the 9 pixels underneath and sums them. The output feature map highlights where edges appear. With 32 filters in the first conv layer, you get 32 different feature maps — one detecting vertical edges, another horizontal edges, another curves, etc.

## Spoken Version
"Convolution is the core operation in CNNs — a small learnable filter slides across the input, detecting local patterns everywhere. It's dramatically more parameter-efficient than fully connected layers because the same filter is reused across the entire image."

## German Workplace Example
"Die Faltung ist die Kernoperation in CNNs. Ein kleiner lernbarer Filter gleitet uber die Eingabe und erkennt lokale Muster uberall im Bild. Das ist viel parametereffizienter als vollvernetzte Schichten."

## Related Concepts
- [[Kernel]]
- [[Feature Map]]
- [[Stride]]
- [[Pooling]]
- [[Neural Networks]]

## Tags
#cnn #convolution #deep-learning #computer-vision
