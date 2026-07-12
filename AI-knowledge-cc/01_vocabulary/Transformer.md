# Transformer

## 是什么
A neural network architecture that processes sequences entirely through self-attention, without any recurrence or convolution. Introduced in "Attention Is All You Need" (Vaswani et al., 2017). Its key innovation: every position in the input can directly attend to every other position, enabling parallel processing and capturing long-range dependencies that RNNs struggle with.

## zh / de
Transformer（变换器）/ der Transformer

## 记住它
> "An RNN is like reading a book word by word, taking notes as you go. A Transformer is like looking at the entire page at once and drawing lines connecting related words — 'it' points to 'the cat,' 'they' points to 'the researchers.' No sequential bottleneck, just direct connections."

## 说
Transformers replaced RNNs as the dominant NLP architecture because they process all positions in parallel via self-attention. The trade-off: quadratic memory in sequence length, but they scale far better with compute and data.

## Tags
#transformer #attention #nlp #deep-learning
