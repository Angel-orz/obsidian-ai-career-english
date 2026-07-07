---
topic: CNN
date: 2026-07-08
---

# Speaking — CNN

## 30-Second Version
"CNNs are the standard neural network architecture for images. Instead of connecting every neuron to every input — which would be millions of parameters — CNNs slide small filters across the image to detect patterns like edges and textures. Pooling layers then downsample, keeping only the strongest signals. The result is a network that learns a hierarchy of visual features, from simple edges to complex objects. They've powered everything from face recognition to self-driving cars for over a decade."

## 60-Second Version
"CNNs revolutionized computer vision by solving the parameter explosion problem. A regular neural network on a 224x224 image would need over 150 million parameters just for the first layer. CNNs use two key ideas: local connectivity — each neuron only looks at a small 3x3 patch — and weight sharing — the same filter is reused across the entire image. This drops parameters to just hundreds per filter.

The architecture stacks three operations: convolution for feature detection, ReLU for non-linearity, and pooling for downsampling. As you go deeper, the spatial resolution shrinks but the number of feature maps grows — the network trades where things are for what things are. Early layers detect edges, middle layers detect shapes, deep layers detect object parts.

In practice, you almost never train a CNN from scratch. You take a ResNet or EfficientNet pre-trained on ImageNet, swap the final classification layer, and fine-tune on your data. This transfer learning approach works even with just a few hundred labeled images."

## Keywords List
| English | Chinese | German |
|---------|---------|--------|
| Convolution | 卷积 | die Faltung |
| Kernel (Filter) | 卷积核 | der Kernel |
| Feature Map | 特征图 | die Feature-Map |
| Pooling | 池化 | das Pooling |
| Stride | 步长 | die Schrittweite |
| Transfer Learning | 迁移学习 | das Transferlernen |
| Receptive Field | 感受野 | das rezeptive Feld |
| Max Pooling | 最大池化 | das Max-Pooling |

## German Summary
CNNs sind die Standardarchitektur fur Computer Vision. Sie verwenden Faltungsschichten, die kleine Filter uber das Bild gleiten lassen, um lokale Muster zu erkennen. Pooling reduziert die Dimensionen, und Transfer Learning ermoglicht den Einsatz mit kleinen Datensatzen.

## Related
- [[CNN]] (02_concepts)
- [[CNN]] (04_meetings)
- [[CNN]] (05_interview)
