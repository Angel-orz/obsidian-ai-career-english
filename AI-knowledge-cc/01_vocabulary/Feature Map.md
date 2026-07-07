# Feature Map

## Definition (English)
A feature map (or activation map) is the output of applying a convolution kernel to an input. Each kernel produces one feature map — a 2D grid where each value indicates how strongly the kernel's pattern matched at that spatial location. Early layers produce feature maps of edges and textures; deeper layers produce feature maps of object parts and whole objects.

## Chinese
特征图

## German
die Feature-Map (die Merkmalskarte)

## Intuition
Imagine highlighting every location in a photo where you see "red." You'd get a heatmap: bright spots where red objects appear, dark elsewhere. A feature map is exactly that — a heatmap showing where a specific pattern was detected. If Kernel #3 detects vertical edges, its feature map lights up wherever vertical edges exist in the image.

## Example
Input: 224x224x3 RGB image → Conv Layer 1 with 64 kernels → 64 feature maps, each 224x224 → Conv Layer 2 with 128 kernels → 128 feature maps, each 112x112. The spatial resolution shrinks (due to pooling/striding), but the number of feature maps grows — the network trades spatial detail for semantic depth.

## Spoken Version
"Each feature map is a spatial heatmap showing where a specific pattern was detected. More kernels = more feature maps = richer representation, at the cost of more computation."

## German Workplace Example
"Jede Feature-Map ist eine raumliche Heatmap, die zeigt, wo ein bestimmtes Muster erkannt wurde. Mehr Kernel bedeuten mehr Feature-Maps und damit eine reichhaltigere Reprasentation."

## Related Concepts
- [[Convolution]]
- [[Kernel]]
- [[Pooling]]
- [[Stride]]

## Tags
#cnn #feature-map #deep-learning
