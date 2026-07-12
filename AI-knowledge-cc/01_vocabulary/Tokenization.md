# Tokenization

## 是什么
The process of splitting raw text into smaller units (tokens) that the model can process. Modern LLMs use subword tokenization (BPE, WordPiece, SentencePiece) — common words like "the" are one token, rare words like "transformer" might be split into ["transform", "er"]. Tokenization is the first step in any NLP pipeline and directly impacts model quality: a poor tokenizer can make a great model fail on rare words or multilingual text.

## zh / de
分词 / die Tokenisierung

## 记住它
> "Tokenization is like breaking a sentence into Lego bricks. 'unbelievable' might be ['un', 'believ', 'able'] — three reusable subword blocks. This is smarter than whole-word tokenization because the model can understand 'unbelievable' even if it never saw that exact word during training. It saw 'un', 'believ', 'able' in other words and can compose their meanings."

## 说
Tokenization is the critical preprocessing step that converts raw text into model-readable tokens. Subword tokenization is the standard because it handles rare words gracefully — splitting them into known subword pieces rather than mapping them to a useless <UNK> token.

## Tags
#tokenization #nlp #preprocessing #bpe
