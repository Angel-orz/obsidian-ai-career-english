# Convolutional Neural Network (CNN)

## Definition (English)
A Convolutional Neural Network (CNN) is a specialized neural network architecture designed primarily for processing grid-like data such as images. Instead of fully connected layers, CNNs use convolution layers that slide learnable filters across the input to detect local patterns — edges, textures, shapes — at every spatial位置. Combined with pooling layers for downsampling and fully connected layers for final classification, CNNs have been the dominant architecture in computer vision since AlexNet's breakthrough in 2012.

## Chinese Explanation
卷积神经网络（CNN）是一种专门用于处理图像等网格数据的神经网络架构。CNN 使用卷积层代替全连接层，通过在输入上滑动可学习的滤波器来检测局部模式——边缘、纹理、形状。结合用于下采样的池化层和用于最终分类的全连接层，自 2012 年 AlexNet 突破以来，CNN 一直是计算机视觉领域的主导架构。

## German Explanation
Ein Convolutional Neural Network (CNN) ist eine spezialisierte neuronale Netzwerkarchitektur, die hauptsachlich fur die Verarbeitung von gitterartigen Daten wie Bildern entwickelt wurde. Anstelle von vollvernetzten Schichten verwenden CNNs Faltungsschichten, die lernbare Filter uber die Eingabe gleiten lassen, um lokale Muster zu erkennen. In Kombination mit Pooling-Schichten und vollvernetzten Schichten sind CNNs seit AlexNet (2012) die dominierende Architektur im Computer Vision.

## Intuition
CNNs solve the key problem with using regular neural networks on images: an image of 224x224x3 pixels has 150,528 input values. A fully connected layer with just 1,000 neurons would need 150 million parameters — impossible to train. CNNs solve this with two insights:

1. **Local connectivity**: A neuron only looks at a small patch (e.g., 3x3), not the whole image. Patterns are local — an edge in the top-left corner follows the same rules as an edge in the bottom-right.
2. **Weight sharing**: The same filter (kernel) is reused across the entire image. Instead of learning "edge detection at position (0,0)" and "edge detection at position (0,1)" separately, one 3x3 kernel (9 parameters) detects edges everywhere.

The architecture naturally builds a hierarchy: Layer 1 detects edges, Layer 2 combines edges into shapes, Layer 3 combines shapes into object parts, Layer 4+ recognizes whole objects.

## How It Works

### Core Building Blocks
1. **Convolution Layer**: Applies K filters (e.g., 32 or 64) to the input. Each filter produces one feature map. Learns to detect specific visual patterns.
2. **Activation Function**: ReLU applied element-wise after convolution. Adds non-linearity.
3. **Pooling Layer**: Max Pooling (2x2, stride 2) downsamples feature maps by 2x. Reduces computation, adds translation invariance.
4. **Fully Connected Layer**: At the end, a few FC layers map the learned visual features to class predictions.

### Typical Architecture Pattern
```
Input (224x224x3)
→ Conv(64 filters, 3x3) + ReLU → 224x224x64
→ MaxPool(2x2) → 112x112x64
→ Conv(128 filters, 3x3) + ReLU → 112x112x128
→ MaxPool(2x2) → 56x56x128
→ Conv(256 filters, 3x3) + ReLU → 56x56x256
→ MaxPool(2x2) → 28x28x256
→ Flatten → FC(512) + ReLU
→ FC(num_classes) + Softmax
```

### Key Innovations
- **AlexNet (2012)**: Proved deep CNNs work on ImageNet. Used ReLU, dropout, GPU training.
- **VGG (2014)**: Showed that deeper = better. Used only 3x3 convolutions, very simple and uniform.
- **ResNet (2015)**: Introduced skip connections — solved the vanishing gradient problem in very deep networks (152 layers!). Became the new standard.
- **EfficientNet (2019)**: Used neural architecture search to find optimal depth/width/resolution balance.

## Real-world Examples
1. **Image Classification** — ResNet-50 classifies 1.2M ImageNet images into 1000 categories. Used in production by every major tech company.
2. **Object Detection** — YOLO and Faster R-CNN use CNN backbones to detect and localize multiple objects in real-time.
3. **Medical Imaging** — CNNs detect tumors in CT scans, diabetic retinopathy in eye images, with accuracy matching or exceeding radiologists.
4. **Self-Driving Cars** — CNNs process camera feeds to detect lanes, traffic signs, pedestrians, and other vehicles.

## Interview Answer
> "CNNs are the standard architecture for computer vision tasks. They address the key limitation of fully connected networks on images through two mechanisms: local connectivity — each neuron only connects to a small spatial region — and weight sharing — the same filter is reused across the entire image. This reduces parameters from hundreds of millions to thousands.
>
> The typical CNN stacks convolution layers (for feature detection), ReLU activations (for non-linearity), and pooling layers (for downsampling and translation invariance). The key hyperparameters are filter size (3x3 is standard), number of filters per layer (doubling as spatial dimensions halve), and depth.
>
> Transfer learning is the practical superpower of CNNs: take a ResNet pre-trained on ImageNet, chop off the final classification layer, add your own classifier, and fine-tune on your specific dataset. This works even with only a few hundred labeled images per class.
>
> The main limitation is that CNNs assume spatial locality — they work great for images but are suboptimal for sequential data or global relationships, which is where Transformers excel. Modern vision is shifting toward Vision Transformers (ViT), but CNNs remain more data-efficient and are still the practical choice for most projects."

## Related Concepts
- [[Convolution]]
- [[Kernel]]
- [[Feature Map]]
- [[Pooling]]
- [[Stride]]
- [[Neural Networks]]
- [[Activation Function]]
- [[Backpropagation]]
- [[Transfer Learning]]
