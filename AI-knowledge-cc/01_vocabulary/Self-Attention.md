# Self-Attention

## 是什么
The core mechanism of Transformers that lets each word in a sequence look at ALL other words simultaneously to compute its representation. Instead of processing step by step like RNNs, self-attention computes weighted relevance scores — "how much should this word pay attention to every other word?"

## zh / de
自注意力 / die Self-Attention (die Selbstaufmerksamkeit)

## 记住它
> "In 'The cat sat on the mat because it was tired,' self-attention connects 'it' to 'cat' by computing that 'cat' is the most relevant word. RNNs would have to carry 'cat' through 6 hidden state steps to make the same link."

## 说
Self-attention is what makes Transformers so powerful — every word can directly attend to every other word, solving the long-range dependency problem that limits RNNs.

## Tags
#transformers #attention #self-attention #deep-learning
