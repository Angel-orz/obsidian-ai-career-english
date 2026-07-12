# Positional Encoding

## 是什么
A technique that injects information about token position into the Transformer's input embeddings. Since self-attention has no inherent sense of order (unlike RNNs which process sequentially), positional encodings tell the model "this word is at position 3." The original Transformer uses sinusoidal functions: PE(pos, 2i) = sin(pos/10000^(2i/d)), PE(pos, 2i+1) = cos(...). Learned positional embeddings or rotary position embeddings (RoPE) are common modern alternatives.

## zh / de
位置编码 / die Positionskodierung

## 记住它
> "Without positional encoding, 'Dog bites man' and 'Man bites dog' look identical to a Transformer — same words, same attention patterns. Positional encoding adds a unique 'address label' to each position so the model knows word order. It's like numbering the words before feeding them in."

## 说
Positional encoding is what gives Transformers a sense of word order — without it, self-attention is permutation-invariant. Sinusoidal encodings were the original approach; learned or rotary position embeddings are now more common.

## Tags
#transformer #positional-encoding #attention #nlp
