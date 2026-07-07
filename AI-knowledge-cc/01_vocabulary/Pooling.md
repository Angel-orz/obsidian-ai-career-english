# Pooling

## Definition (English)
Pooling is a downsampling operation that reduces the spatial dimensions of feature maps by summarizing local regions. Max Pooling takes the maximum value in each small window (e.g., 2x2), discarding the rest. This reduces computation for deeper layers, provides translation invariance, and forces the network to learn the most important features rather than precise positions.

## Chinese
池化

## German
das Pooling (die Bundelung)

## Intuition
Think of zooming out on Google Maps. At street level, you see every detail. At city level, you see only the major roads — the details are summarized. Max Pooling does this: it takes a 2x2 region and keeps only the strongest signal. This shrinks the feature map from 112x112 to 56x56, cutting computation by 75% for the next layer.

## Example
Max Pooling with 2x2 window: [1,3 / 2,1] → max = 3; [2,4 / 5,1] → max = 5; [4,2 / 1,5] → max = 5; [6,8 / 3,2] → max = 8. Each 2x2 region replaced by its maximum — half the dimensions, 75% smaller.

## Spoken Version
"Max pooling aggressively downsamples feature maps — keep only the strongest activation in each small region. It reduces computation, adds robustness to small translations, and helps prevent overfitting."

## German Workplace Example
"Max Pooling reduziert die raumlichen Dimensionen der Feature-Maps drastisch — es behalt nur die starkste Aktivierung in jeder kleinen Region. Das spart Rechenleistung und macht das Netzwerk robuster gegenuber kleinen Verschiebungen."

## Related Concepts
- [[Convolution]]
- [[Feature Map]]
- [[Stride]]

## Tags
#cnn #pooling #downsampling #deep-learning
