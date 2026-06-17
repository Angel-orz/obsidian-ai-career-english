# Practice Dialog — Recommendation System Meeting

**Scenario:** Team meeting about a new product recommendation system

---

**Alice (PM):** "We need a recommendation engine for our e-commerce platform. How should we approach this?"

**You:** "This sounds like a supervised learning problem. We need historical purchase data as labels — what users actually bought. The features would be user behavior, product categories, browsing history. What kind of labeled data do we already have available?"

**Bob (Data Engineer):** "We have about 500,000 past transactions with user and product info."

**You:** "That's a solid starting point. I'd suggest we split that into train and test sets, start with a collaborative filtering baseline, and evaluate with a ranking metric like NDCG. In my experience, for this kind of problem with reasonable data volume, starting with a simpler model first helps us establish a baseline before we explore deep learning approaches."

**Alice:** "How long would that take?"

**You:** "Let me think about it — with the data already available, a baseline model should be doable within a week. Could you elaborate on the performance requirements? That would help me give a more accurate timeline."

---

## Phrases Used
- [[Asking Questions]] — "What kind of labeled data do we already have available?"
- [[Giving Opinions]] — "I'd suggest we split that into train and test sets..."
- [[Buying Time]] — "Let me think about it..."
