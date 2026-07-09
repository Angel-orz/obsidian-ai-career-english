---
date: 2026-07-09
topic: RNN & Transformers Intro
---

# RNN & Transformers Intro | 2026-07-09

## 📝 今日 3 词
| 词 | 一句话定义 | zh / de |
|----|-----------|---------|
| [[Sequential Data]] | Data where order matters — text, audio, time series | 序列数据 / sequenzielle Daten |
| [[Hidden State]] | RNN's memory vector that carries info from previous steps forward | 隐藏状态 / der Hidden State |
| [[Self-Attention]] | Each word looks at ALL other words simultaneously to compute relevance | 自注意力 / die Self-Attention |

## 🗣 30 秒说出来
RNNs and Transformers both handle sequential data, but in completely different ways. An RNN reads input step by step, maintaining a hidden state as memory — like reading a book one word at a time and keeping notes. The problem: on long sequences, the memory fades. Transformers solve this with self-attention — every word looks at every other word simultaneously. Instead of carrying information through dozens of steps like an RNN, a Transformer just directly connects related words. This parallel processing is why Transformers train much faster and handle long-range dependencies better. The trade-off: Transformers need more compute and data, but for most NLP tasks today, they're the default choice.

## 🇩🇪 德文一句
"RNNs verarbeiten Sequenzen Schritt fur Schritt mit einem Hidden State als Gedachtnis. Transformers ersetzen das durch Self-Attention — jedes Wort kann direkt auf alle anderen zugreifen. Dadurch sind sie paralleler und schneller trainierbar."

## 🎤 快问快答
**Q:** Why did Transformers replace RNNs as the dominant architecture for NLP?
**A:** Three reasons: (1) Parallel training — RNNs must process sequentially, Transformers process all positions at once. (2) Long-range dependencies — self-attention connects any two words directly, RNNs lose information over long sequences. (3) Scalability — Transformers scale better with more data and compute. The cost: quadratic memory in sequence length, and they need more training data to match RNN performance on small datasets.

## 🔁 回顾（前天 — CNN, 7月8日）
- [ ] Convolution — 滤波器在图像上滑动，逐元素相乘再求和...
- [ ] Kernel — 3×3的可学习权重矩阵，作为模式检测器...
- [ ] Pooling — 下采样，在每个2×2区域只保留最大值...
