# Query-Key-Value

## 是什么
The three learned projections at the heart of the attention mechanism. Each input token is linearly projected into three vectors: Query (Q — "what am I looking for?"), Key (K — "what do I contain?"), and Value (V — "what information do I pass on?"). Attention scores are computed as similarity(Q, K), then used to weight the Values. All three are learned during training. In self-attention, Q, K, V all come from the same input sequence (projected differently); in cross-attention, Q comes from the Decoder, K and V from the Encoder.

## zh / de
查询-键-值 / Query-Key-Value (QKV)

## 记住它
> "Think YouTube search: Your search query = Q, video titles = K, video content = V. The system computes which titles best match your query (Q·K^T), ranks them with softmax, then serves you the most relevant videos (weighted sum of V). In attention, every token creates its own Q, K, and V projections — each position queries all others for relevant information."

## 说
QKV is the retrieval metaphor behind attention: Query asks "what's relevant?", Key advertises "here's what I have," and Value delivers the actual content. In self-attention, every token projects into all three roles simultaneously — it's querying, being queried, and delivering information to others all at once.

## Tags
#attention #transformer #qkv #deep-learning
