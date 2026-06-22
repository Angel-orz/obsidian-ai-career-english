---
topic: Neural Networks
date: 2026-06-20
---

# Meeting English — Neural Networks

## Asking Questions
> "How many hidden layers do you think we need for this problem, given the amount of training data we have?"
> *Use when: Scoping network architecture with the team*

> "Are we more concerned about training speed or final accuracy here?"
> *Use when: Deciding between a shallow fast network and a deep accurate one*

## Clarifying
> "When you say the model is overfitting, are you seeing a large gap between training and validation loss?"
> *Use when: Diagnosing overfitting symptoms reported by a teammate*

> "Should we try dropout first, or add more training data — which is more feasible given our timeline?"
> *Use when: Choosing between regularization strategies*

## Giving Opinions
> "I'd start with two hidden layers and ReLU activation — it's a solid baseline for tabular data. We can go deeper if the data supports it."
> *Use when: Proposing a pragmatic starting architecture*

> "In my experience, for this dataset size, a wider network with dropout tends to generalize better than a deeper one without regularization."
> *Use when: Recommending architecture based on data volume*

## Agreeing
> "Exactly — the learning rate is the most important hyperparameter to tune first. Everything else can wait."
> *Use when: Aligning on hyperparameter tuning priority*

## Buying Time
> "Let me check the training curves before I answer — I want to see if the loss has plateaued or if we just need more epochs."
> *Use when: Asked about model readiness, need to verify training progress*

## Practice Dialog — Model Design Discussion
**Scenario:** Team discussion about building a defect detection model for a manufacturing line.

**You:** "For this defect detection task, I'd recommend starting with a relatively simple architecture — maybe 3 hidden layers with 128, 64, and 32 neurons respectively, using ReLU activation."

**Colleague:** "Why not go deeper? Don't deeper networks perform better?"

**You:** "They can, but deeper networks need more data to generalize well. We have about 5,000 labeled images — that's enough for a moderate network but not enough for something like ResNet-50 from scratch. I'd rather start simple, establish a baseline, and add complexity if we see underfitting. How does that sound?"

## Related
- [[Neural Networks]] (03_speaking)
- [[Neural Networks]] (05_interview)
