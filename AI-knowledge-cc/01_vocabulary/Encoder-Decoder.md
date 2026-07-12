# Encoder-Decoder

## 是什么
A two-part architecture where the Encoder processes the input sequence into a dense representation (context), and the Decoder generates the output sequence from that context. The original Transformer uses 6 encoder layers + 6 decoder layers. The encoder builds a rich representation of the input; the decoder uses cross-attention to focus on relevant parts of the encoded input while generating each output token.

## zh / de
编码器-解码器 / der Encoder-Decoder (der Kodierer-Dekodierer)

## 记住它
> "The Encoder reads and understands the source sentence: 'Je suis etudiant.' It builds a rich representation capturing grammar, meaning, and context. The Decoder writes the translation one word at a time: 'I... am... a... student.' At each step, the Decoder looks back at the Encoder's output via cross-attention — 'when generating the third word, which French words matter most?'"

## 说
The encoder-decoder split is the foundation of sequence-to-sequence models. The encoder builds a representation; the decoder generates output step by step, attending back to the encoder at each step via cross-attention.

## Tags
#transformer #encoder-decoder #seq2seq #nlp
