---
topic: CNN
date: 2026-07-08
---

# Interview — CNN

## Question
> "Explain how a CNN works. Why are CNNs better than fully connected networks for images? Give a concrete example."

## 30-Second Answer
"CNNs use convolution layers that slide small learnable filters across the image to detect local patterns. This is far more efficient than fully connected layers because of local connectivity and weight sharing — a 3x3 filter has just 9 parameters but can detect edges anywhere in the image. Pooling layers then downsample, and stacking these operations builds a hierarchy from edges to shapes to objects. Transfer learning from pre-trained models like ResNet makes CNNs practical even with small datasets."

## Strong Answer
"CNNs solve two fundamental problems with applying regular neural networks to images.

First, **parameter efficiency**. A 224x224x3 image has 150,528 pixels. A fully connected layer with 1,000 neurons would need 150 million parameters — and that's just the first layer. CNNs use local connectivity — each neuron connects to only a 3x3 spatial region — and weight sharing — the same 9-parameter filter is reused across the entire image. A conv layer with 64 filters needs only 64 x (3x3x3 + 1) = 1,792 parameters.

Second, **spatial structure**. Fully connected layers flatten the image, destroying all spatial information. CNNs preserve the 2D grid structure, allowing filters to detect spatial patterns. This enables the hierarchical feature learning that makes CNNs so effective: Layer 1 detects edges, Layer 2 detects shapes, Layer 3 detects object parts, Layer 4+ recognizes objects.

The architecture has three core operations repeated in blocks: convolution (feature detection) → ReLU (non-linearity) → Pooling (downsampling). As you go deeper, spatial dimensions shrink while the number of feature maps grows — the network trades spatial precision for semantic richness.

In practice, I almost always use transfer learning: take a ResNet or EfficientNet pre-trained on ImageNet, remove the final classification head, add my own, and fine-tune. This works with as few as a few hundred labeled images because the early layers' edge and texture detectors generalize across almost all visual tasks. I freeze early layers and only fine-tune the later ones when data is limited; with more data, I unfreeze more layers."

## Common Mistakes
1. **Training from scratch** with small data — use transfer learning unless you have millions of images
2. **Wrong input size** — pre-trained models expect specific resolutions (224x224 for ResNet, 299x299 for Inception)
3. **Not applying the same pre-processing** as the pre-trained model — ImageNet normalization (mean=[0.485, 0.456, 0.406], std=[0.229, 0.224, 0.225]) is required
4. **Using too large a learning rate during fine-tuning** — pre-trained weights are already good, use 10x smaller LR than training from scratch
5. **Ignoring data augmentation** — random flips, rotations, and color jitter are essentially free training data

## Related
- [[CNN]] (02_concepts)
- [[CNN]] (03_speaking)
