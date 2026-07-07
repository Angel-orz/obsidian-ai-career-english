# Stride

## Definition (English)
Stride is the step size by which a filter moves across the input during convolution or pooling. A stride of 1 means the filter moves one pixel at a time (dense coverage, larger output). A stride of 2 means it jumps two pixels each time (sparser coverage, halved output dimensions). Larger strides aggressively downsample.

## Chinese
步长

## German
die Schrittweite (der Stride)

## Intuition
Imagine reading a book with your finger tracking each word. Reading every word = stride 1 (slow, thorough). Reading every other word = stride 2 (faster, but might miss nuance). In CNNs, stride controls the trade-off between spatial resolution and computational cost. Early layers use stride 1 to preserve detail; later layers may use stride 2 to downsample.

## Example
A 3x3 kernel with stride 1 over a 32x32 input produces a 30x30 output. Same kernel with stride 2: output = (32-3)/2 + 1 = 15. The output is roughly half the size, computation roughly halved. In ResNet, the first layer often uses stride 2 to immediately downsample.

## Spoken Version
"Stride controls how densely the filter scans the input. Stride 1 gives full coverage; stride 2 halves the output dimensions and roughly halves computation, acting as a form of downsampling alongside pooling."

## German Workplace Example
"Die Schrittweite steuert, wie dicht der Filter die Eingabe abtastet. Schrittweite 1 gibt vollstandige Abdeckung; Schrittweite 2 halbiert die Ausgabedimensionen und reduziert den Rechenaufwand erheblich."

## Related Concepts
- [[Convolution]]
- [[Kernel]]
- [[Pooling]]
- [[Feature Map]]

## Tags
#cnn #stride #downsampling #deep-learning
