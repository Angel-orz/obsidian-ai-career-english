---
date: 2026-07-10
topic: Transformer Architecture
---

# Transformer Architecture | 2026-07-10

## 📝 今日 3 词
| 词 | 一句话定义 | zh / de |
|----|-----------|---------|
| [[Transformer]] | Architecture that processes sequences via self-attention — no recurrence, fully parallel | Transformer / der Transformer |
| [[Encoder-Decoder]] | Encoder builds rich input representation; Decoder generates output step-by-step with cross-attention | 编码器-解码器 / der Encoder-Decoder |
| [[Positional Encoding]] | Injects position info into input so the model knows word order, since attention is order-blind | 位置编码 / die Positionskodierung |

## 🗣 30 秒说出来
The Transformer architecture, introduced in the 'Attention Is All You Need' paper, fundamentally changed NLP. It replaces recurrence with self-attention — instead of processing words one by one like an RNN, every word can directly attend to every other word. The architecture has two parts: an Encoder that builds a rich understanding of the input, and a Decoder that generates output one token at a time while attending back to the Encoder. Since attention doesn't inherently know word order, positional encodings are added to give each token a unique position label. This design enables massive parallelization during training, which is why we can train models like GPT and BERT on internet-scale data.

## 🇩🇪 德文一句
"Der Transformer ersetzt rekurrente Verarbeitung durch Self-Attention — jedes Wort kann direkt auf jedes andere zugreifen. Encoder und Decoder arbeiten mit paralleler Aufmerksamkeit, und Positionskodierungen verleihen dem Modell ein Gefuhl fur die Wortreihenfolge."

## 🎤 快问快答
**Q:** What are the three core components of the Transformer architecture?
**A:** (1) Self-Attention — lets each position attend to all positions, computing relevance scores. (2) Position-wise Feed-Forward Networks — applied identically to each position after attention. (3) Positional Encoding — injects sequence order information. Plus residual connections and layer normalization around each sub-layer for stable deep training.

## 🔁 回顾（昨天 — RNN & Transformers Intro, 7月9日）
- [ ] Sequential Data — 顺序重要的数据...
- [ ] Hidden State — RNN的记忆向量...
- [ ] Self-Attention — 每个词同时关注所有词...
