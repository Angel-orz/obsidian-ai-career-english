# Embedding

## 是什么
A dense, low-dimensional vector representation of a discrete token (word, subword, or even an entire sentence). Instead of representing "cat" as a sparse one-hot vector of size 50,000, an embedding compresses it into a dense vector of size 300-4096. The key property: semantically similar words have similar vectors — "cat" and "kitten" are close in embedding space. Modern LLMs learn embeddings as the first layer, and these vectors are the "language" that all subsequent layers operate on.

## zh / de
嵌入（词向量）/ das Embedding (die Einbettung)

## 记住它
> "One-hot encoding: 'cat' = [0,0,0,1,0,...,0] — 50,000 zeros and one 1. Tells you nothing about 'cat' vs 'kitten.' Embedding: 'cat' = [0.23, -0.71, 0.04, ..., 0.15] — 768 numbers that capture meaning. Now 'cat' - 'kitten' + 'puppy' ≈ 'dog.' Embeddings turn discrete words into a continuous semantic space where arithmetic on meaning is possible."

## 说
Embeddings are the bridge between discrete tokens and continuous neural networks — they map words into a dense semantic space where similar meanings cluster. The embedding layer is the first thing every LLM learns, and the quality of these vectors determines everything downstream.

## Tags
#embedding #nlp #representation #word2vec
