---
tags: [daily-notes]
topic: CNN
date: 2026-07-08
---

# Daily Notes — CNN

## Vocabulary Learned
- [ ] [[Convolution]]
- [ ] [[Kernel]]
- [ ] [[Feature Map]]
- [ ] [[Pooling]]
- [ ] [[Stride]]

## Concepts Learned
| Concept | Understanding (1-5) | Notes |
|---------|---------------------|-------|
| Convolution operation | 4 | Filter slides, element-wise multiply + sum |
| Weight sharing & parameter efficiency | 5 | 3x3x64 = 576 params vs millions in FC |
| Hierarchical feature learning | 4 | Edges → shapes → objects |
| Pooling for downsampling | 5 | Max pool 2x2: keep strongest, 75% smaller |
| Transfer learning | 4 | Pre-trained ResNet + custom head + fine-tune |
| CNN vs ViT trade-off | 3 | CNNs more data-efficient; ViTs need more data |

## Speaking Practice
| Exercise | Completed | Self-Rating |
|----------|-----------|-------------|
| 30-second CNN explanation | [ ] | — |
| 60-second detailed explanation | [ ] | — |
| German workplace scenario | [ ] | — |

## Difficulties
- CNN vs Vision Transformer trade-offs need deeper understanding — when exactly does ViT surpass CNN?
- Receptive field calculation through multiple layers — need to work through an example

## Reflection
- The key insight is weight sharing: CNNs don't just reduce parameters — they bake in the inductive bias that patterns are translation-invariant. This is what makes them data-efficient.
- Transfer learning is the practical superpower — almost nobody trains CNNs from scratch anymore.

## Next Steps
- [ ] Review vocabulary (spaced repetition)
- [ ] Watch 3Blue1Brown CNN video for visual intuition
- [ ] Preview next topic: RNN & Transformers Intro
