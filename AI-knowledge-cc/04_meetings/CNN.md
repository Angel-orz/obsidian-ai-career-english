---
topic: CNN
date: 2026-07-08
---

# Meeting English — CNN

## Asking Questions
> "Should we train from scratch or use a pre-trained model and fine-tune — how much labeled data do we have?"
> *Use when: Starting a computer vision project*

> "What's the inference latency budget? That'll determine whether we can use a large model like ResNet-152 or need something lighter like MobileNet."

## Clarifying
> "When you say the model is struggling with small objects, are they small in absolute pixels or small relative to the image size?"
> *Use when: Diagnosing detection failures*

> "Are we optimizing for top-1 accuracy or top-5? For this use case, top-5 might be acceptable."

## Giving Opinions
> "I'd start with a pre-trained ResNet-50 as backbone — it's the most battle-tested architecture, and there are solid implementations in every framework."
> *Use when: Recommending a CNN architecture*

> "Given our small dataset, I strongly recommend transfer learning. Freeze the early layers and only fine-tune the last few — that prevents overfitting when you have limited data."

## Agreeing
> "Exactly — data augmentation is essentially free training data for CNNs. Random flips, rotations, and color jitter can easily double our effective dataset size."

## Buying Time
> "Let me check the model zoo to see which pre-trained weights are available for that architecture before I commit to a recommendation."

## Practice Dialog — Architecture Selection
**You:** "For this defect detection task, I recommend starting with a pre-trained ResNet-50. It's well-tested, and there are official weights for PyTorch and TensorFlow."

**Manager:** "Why not use the latest Vision Transformer? I've heard they're better."

**You:** "They can be, but ViTs typically need more data — often millions of images — to match CNN performance. With our 5,000 labeled images, a fine-tuned CNN will likely outperform a ViT. Transfer learning from ImageNet gives us a huge head start — the model already knows what edges and shapes look like. We just teach it what defects look like."

## Related
- [[CNN]] (03_speaking)
- [[CNN]] (05_interview)
