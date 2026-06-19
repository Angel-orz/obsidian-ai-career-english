---
topic: Classification & Regression
date: 2026-06-19
---

# Meeting English — Classification & Regression

## Asking Questions

> **"Before we jump into modeling, should we frame this as a classification or a regression problem?"**
> *Use when: Starting a new ML project and scoping the approach with the team*

> **"What's the business cost of a false positive versus a false negative here?"**
> *Use when: Discussing which classification metric to optimize*

> **"Do we care more about being exactly right on the number, or about getting the direction right?"**
> *Use when: Deciding whether regression precision or trend accuracy matters more*

## Clarifying

> **"When you say 'we need to predict customer value,' do you mean a specific euro amount, or a tier like high/medium/low?"**
> *Use when: Stakeholder describes the problem ambiguously — clarify classification vs. regression*

> **"Are the classes balanced, or do we have a heavy skew toward one category?"**
> *Use when: Suspecting class imbalance that would make accuracy misleading*

> **"Is the target truly continuous, or is it actually discrete values that just happen to be numbers — like ratings 1 through 5?"**
> *Use when: Determining if a numeric target should be treated as ordinal classification*

## Giving Opinions

> **"I'd recommend starting with logistic regression as a baseline — it's fast, interpretable, and gives us calibrated probabilities. We can always move to a more complex model later."**
> *Use when: Proposing a practical approach to binary classification*

> **"In my experience, for tabular data with this many features, gradient boosting usually outperforms linear regression. I'd suggest we benchmark both."**
> *Use when: Recommending regression approach based on data characteristics*

> **"I think we should frame this as a classification problem with a custom threshold rather than pure regression — the business decision only cares whether the value is above or below a cutoff."**
> *Use when: Suggesting reframing regression as classification for better business alignment*

## Agreeing

> **"Exactly — accuracy would be misleading here with only 2% fraud cases. We should optimize for recall even if precision takes a hit."**
> *Use when: Aligning on metric choice for imbalanced classification*

> **"Good point. Since the target is a rating on a 1-10 scale, treating it as regression preserves the ordering information that one-hot classification would lose."**
> *Use when: Agreeing on regression for ordinal targets*

> **"I completely agree. Let's start simple with linear regression and MAE, then iterate — no need to jump to neural networks on day one."**
> *Use when: Supporting an incremental complexity approach*

## Buying Time

> **"That's a good question — let me think about whether RMSE or MAE makes more sense given how sensitive the business is to outliers in the prediction."**
> *Use when: You need a moment to choose the right error metric*

> **"Could you clarify what action the team will take based on this prediction? That'll help me decide whether we need hard classifications or probability scores."**
> *Use when: You need business context before choosing between hard/soft classification*

> **"Let me quickly check the class distribution in our training data before I commit to a specific evaluation metric."**
> *Use when: You want to verify data balance before recommending metrics*

## Practice Dialog — Project Scoping Meeting

**Scenario:** Scoping meeting with the product team for a new customer retention feature.

**Marcus (Product Manager):** "We want to predict which customers are at risk of leaving so we can offer them retention deals. Can ML help with this?"

**You:** "Absolutely — this is a classic binary classification problem. We'd predict 'will churn' or 'won't churn' for each customer. Before we jump into modeling, what's the business cost of a false positive versus a false negative here?"

**Marcus:** "A false positive means we offer a discount to someone who would have stayed anyway — that costs us margin. A false negative means we miss someone who actually leaves — that costs us the entire customer. So missing a churner is much worse."

**You:** "That's really helpful. Given that, we should optimize for recall over precision — we'd rather annoy a few loyal customers with unnecessary discounts than lose churners. I'd recommend starting with logistic regression as a baseline — it's fast, interpretable, and gives us calibrated probabilities we can threshold to balance those costs."

**Marcus:** "What kind of accuracy can we expect?"

**You:** "Accuracy would be misleading here — churners are probably only 5-10% of your customer base. A model that predicts 'no churn' for everyone would be 90-95% accurate but completely useless. We'll track precision, recall, and F1-score instead. The confusion matrix will show us exactly how many churners we're catching and how many false alarms we're raising. Let me verify the class distribution first and get back to you with a concrete plan."

## Related
- [[Classification & Regression]] (03_speaking)
- [[Classification & Regression]] (05_interview)
