# Word2Vec

## 是什么
A pioneering word embedding method (Mikolov et al., 2013) that learns vector representations by predicting context: given a word, predict surrounding words (Skip-gram), or given surrounding words, predict the center word (CBOW). Trained on large corpora, it produces embeddings where vector arithmetic captures semantic relationships — the famous "king - man + woman ≈ queen." While modern LLMs use more sophisticated embeddings, Word2Vec established the core idea that meaning can be encoded in dense vectors.

## zh / de
Word2Vec / das Word2Vec

## 记住它
> "Word2Vec proved that you could learn word meanings just by playing a prediction game: 'Can you guess the word from its neighbors?' After millions of guesses on Wikipedia, the model's internal vectors naturally captured that Paris:France :: Berlin:Germany, and king - man + woman ≈ queen. No one told it these relationships — they emerged from the prediction task."

## 说
Word2Vec demonstrated that dense vector representations trained on a simple prediction objective naturally capture semantic relationships. It paved the way for all modern embedding approaches, from GloVe to BERT to GPT's token embeddings.

## Tags
#embedding #word2vec #nlp #representation
