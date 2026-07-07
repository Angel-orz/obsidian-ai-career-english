# Kernel

## Definition (English)
A kernel (or filter) is a small matrix of learnable weights used in convolution operations. It slides across the input, and at each position, an element-wise multiplication and sum produces one output value. A CNN layer typically has multiple kernels (e.g., 32 or 64), each learning to detect a different pattern.

## Chinese
卷积核（滤波器）

## German
der Kernel (der Filter, der Faltungskern)

## Intuition
Think of kernels as "pattern detectors." One kernel might detect horizontal edges: its weights look like [-1,-1,-1 / 0,0,0 / +1,+1,+1]. Another might detect a specific texture. During training, the network discovers which patterns are useful and adjusts each kernel's 9 numbers accordingly. You never tell the kernel "detect edges" — it figures that out from data.

## Example
In a face detection CNN: Kernel 1 learns vertical edges (nose bridge), Kernel 2 learns horizontal edges (eyebrows), Kernel 5 learns eye-like patterns (dark circle surrounded by lighter skin). After training on thousands of faces, these kernels self-organize into a hierarchy of visual detectors.

## Spoken Version
"A kernel is just a tiny grid of numbers — typically 3x3 — that acts as a pattern detector. The magic is that CNNs learn the kernel values automatically from data, so you don't hand-craft feature detectors."

## German Workplace Example
"Ein Kernel ist im Grunde ein winziges Zahlenraster — typischerweise 3x3 — das als Musterdetektor fungiert. CNNs lernen die Kernel-Werte automatisch aus den Daten."

## Related Concepts
- [[Convolution]]
- [[Feature Map]]
- [[Stride]]
- [[Weights]]

## Tags
#cnn #kernel #filter #deep-learning
