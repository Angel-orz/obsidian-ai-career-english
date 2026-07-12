---
date: 2026-07-12
topic: Attention Mechanism
---

# Attention Mechanism | 2026-07-12

## 📝 今日 3 词
| 词 | 一句话定义 | zh / de |
|----|-----------|---------|
| [[Attention Mechanism]] | Dynamic weighted sum over all input positions — focus on what matters, ignore what doesn't | 注意力机制 / der Aufmerksamkeitsmechanismus |
| [[Query-Key-Value]] | Q = "what do I need?", K = "what do I have?", V = "here's my info" — the retrieval triple behind attention | 查询-键-值 / Query-Key-Value |
| [[Multi-Head Attention]] | Run multiple attention operations in parallel, each learning different relationships, then merge all outputs | 多头注意力 / die Multi-Head-Attention |

## 🗣 30 秒说出来
Attention is the 'secret sauce' of Transformers. It's a mechanism that lets every position in a sequence dynamically focus on every other position. The math is straightforward: each token projects into three vectors — Query, Key, and Value. The Query asks 'what am I looking for?', the Key says 'here's what I contain,' and their dot product gives a relevance score. Softmax normalizes these scores into attention weights, which are then used to compute a weighted sum of the Values. Multi-head attention runs this process in parallel with 8 or more different learned projections — each head can specialize in different relationships, like one tracking subject-verb agreement and another tracking pronoun references. The scaled dot-product attention formula — softmax(QK^T / sqrt(d_k)) × V — is arguably the most important equation in modern AI.

## 🇩🇪 德文一句
"Der Aufmerksamkeitsmechanismus berechnet Relevanzwerte zwischen allen Positionen und erzeugt eine gewichtete Summe. Multi-Head-Attention fuhrt diesen Prozess mehrfach parallel durch — jeder Kopf lernt andere Beziehungen, von Grammatik bis Koreferenz."

## 🎤 快问快答
**Q:** Why scale the dot product by √d_k in the attention formula?
**A:** Without scaling, dot products Q·K^T grow large in magnitude as d_k increases (e.g., d_k=64 means dot products span a wide range). Large values push softmax into regions with extremely small gradients — the "saturated softmax" problem, where attention becomes nearly one-hot and gradients vanish. Dividing by √d_k keeps the variance ~1, keeping softmax in a well-behaved region with meaningful gradients.

## 🔁 回顾（昨天 — Embeddings, 7月11日）
- [ ] Embedding — 把离散词映射到连续语义空间...
- [ ] Word2Vec — 通过预测上下文学习词向量...
- [ ] Tokenization — 把文本切分成子词单元...
