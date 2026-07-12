# Multi-Head Attention

## 是什么
Instead of computing one attention function, Multi-Head Attention runs multiple attention operations in parallel ("heads"), each with its own learned Q, K, V projections. Each head can specialize in different relationships — one head might track subject-verb agreement, another coreference resolution, another sentiment. The outputs of all heads are concatenated and projected back to the model dimension. Typical: 8-96 heads depending on model size.

## zh / de
多头注意力 / die Multi-Head-Attention

## 记住它
> "Single-head attention is like reading a sentence looking only for one type of relationship — say, subject-verb agreement. Multi-head attention is like reading the same sentence with 8 different colored highlighters, each tracking a different thing: one for grammar, one for pronouns, one for sentiment, one for temporal order. Then you combine all the highlights into one rich understanding. Each head learns its specialty autonomously during training."

## 说
Multi-head attention lets the model attend to different relationship types simultaneously — at the same position, one head tracks syntax while another tracks semantics. It's like having 8+ parallel attention functions, each with its own perspective, whose outputs are then merged.

## Tags
#attention #transformer #multi-head #deep-learning
