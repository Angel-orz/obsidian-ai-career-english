# Hidden State

## 是什么
A vector that acts as the "memory" of an RNN, carrying information from previous time steps forward. At each step, the hidden state is updated based on the new input AND the previous hidden state. Too long a sequence → the memory fades (vanishing gradient).

## zh / de
隐藏状态 / der Hidden State (der versteckte Zustand)

## 记住它
> "An RNN reading 'I grew up in France... I speak fluent...' uses its hidden state to remember 'France' so it can predict 'French.' The hidden state is what gives RNNs their memory — and also their biggest weakness on long sequences."

## 说
The hidden state is the RNN's memory mechanism — it's updated at each step but degrades over long sequences, which is exactly the problem Transformers solve with attention.

## Tags
#rnn #hidden-state #sequential #deep-learning
