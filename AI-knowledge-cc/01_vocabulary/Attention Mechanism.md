# Attention Mechanism

## 是什么
A technique that lets a model dynamically focus on the most relevant parts of the input when producing each output. Instead of compressing the entire input into a fixed-size vector (like early seq2seq models), attention computes a weighted sum over all input positions, where the weights reflect relevance. The key formula: Attention(Q,K,V) = softmax(QK^T / √d_k) × V — compute similarity scores, normalize with softmax, use as weights for a weighted sum.

## zh / de
注意力机制 / der Aufmerksamkeitsmechanismus

## 记住它
> "Imagine translating a long German sentence where the verb is at the very end. An RNN with no attention has compressed all 50 words into one fixed vector — by the time it reaches the end, it's 'forgotten' the subject. Attention lets the model look back: 'I'm generating the English verb now — which German words should I look at?' It connects distant parts of a sentence directly, bypassing the sequential bottleneck."

## 说
Attention is the core innovation behind Transformers. It computes relevance scores between every pair of positions, then creates a weighted combination — letting the model dynamically focus on what matters. The √d_k scaling prevents dot products from growing too large in high dimensions.

## Tags
#attention #transformer #nlp #deep-learning
