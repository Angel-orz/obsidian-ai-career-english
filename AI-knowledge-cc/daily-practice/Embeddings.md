---
date: 2026-07-11
topic: Embeddings
---

# Embeddings | 2026-07-11

## 📝 今日 3 词
| 词 | 一句话定义 | zh / de |
|----|-----------|---------|
| [[Embedding]] | Dense vector that maps discrete tokens into a continuous semantic space where similar meanings cluster | 嵌入 / das Embedding |
| [[Word2Vec]] | Pioneering method (2013) that learns word vectors by predicting context — proved king - man + woman ≈ queen | Word2Vec / das Word2Vec |
| [[Tokenization]] | Splitting text into model-readable subword units — "transformer" → ["transform", "er"] | 分词 / die Tokenisierung |

## 🗣 30 秒说出来
Embeddings are how neural networks understand language. Instead of representing words as sparse one-hot vectors — 50,000 dimensions with a single 1 and 49,999 zeros — embeddings compress each word into a dense vector of, say, 768 numbers. The beauty is that these vectors capture meaning: similar words have similar vectors, and you can do arithmetic — king minus man plus woman gives you something close to queen. Word2Vec first proved this in 2013 by training on a simple prediction task: guess a word from its neighbors. Today, every LLM starts with a tokenizer that splits text into subword pieces and an embedding layer that converts those pieces into vectors. Tokenization quality directly impacts the model — a bad tokenizer means the embedding layer gets garbage, and garbage in means garbage out.

## 🇩🇪 德文一句
"Embeddings sind dichte Vektoren, die diskrete Worter in einen kontinuierlichen semantischen Raum abbilden. Ahnliche Bedeutungen liegen nah beieinander. Word2Vec hat 2013 gezeigt, dass Vektorarithmetik semantische Beziehungen abbilden kann — Konig minus Mann plus Frau ≈ Konigin."

## 🎤 快问快答
**Q:** Why do we use embeddings instead of one-hot encoding?
**A:** Three reasons: (1) Dimensionality — one-hot for a 50K vocabulary is 50K dimensions per word; embeddings compress to 300-4096 dimensions. (2) Semantics — one-hot vectors are orthogonal (all equally different), embeddings capture similarity. (3) Generalization — embeddings let the model transfer knowledge between related words; if it understands "good," it partially understands "great" before seeing it.

## 🔁 回顾（昨天 — Transformer Architecture, 7月10日）
- [ ] Transformer — 通过Self-Attention处理序列...
- [ ] Encoder-Decoder — Encoder编码输入，Decoder生成输出...
- [ ] Positional Encoding — 注入位置信息...
