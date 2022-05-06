# Non-Personalised
Top average - IMBD tier list.
# Supervised
- Add non category interests.
# User based:
# Candidate Generation
- Personalised (personality, goals), contextualised (time, place).
- Engineer joy!
- Items are interacted with.
- Features: defined by domain expert: categories, keywords.
- Users: vector U. Features: age, sex.
- User-Item Interactions. UxI = R
- Sparsity - hard to find similar rows 1-(entries/uxI)
- Cold-start - items: no ratings - users.
# Scoring
- Domaim-specific
- Q: feature dim d: d x I - item features
- P: U x d - User interest in features
- Similarity is Pu x Qu.
- Collaborative Filtering 
### User based nearest neighbours
- Cosine similarity pearson correlation.
- Mean of neighbours ratings of i.
- Weighted mean - weights are similarities.
- Advantages - No item/user features - collected passively.
- Serendipity
- Disadvantages - slow, cold-start bad, may not be able to explaine results.
- User-based
### Matrix factorisation
- Model based
- R is sparse due to U x I
- Embeddings - maps sparse vectors to dense vectors.
- vector P - row for each user columns d.
- vector Q - column for each item - row d.
- ^rui = PuQi.
- Latent features - learning embeddings
- Learn how much each feature is represented over time in Q items via SGD.
- Matrix completion.
- Learning embeddings takes time
# Top-N recommendation
### Diversity
-  Require min distance between top N
- Greedy re-ranking: select N that achieve best balance between relevance and diver
## Serendipity
- Pleasure
## Novelity
- Non-popular
## Diversity
- Different tastes

# Prediction
- Implicit: clicked/dload/purchase
- Not easy to infer negative opinions
# Context-Aware
- Pre-filter irrelevant.
- Post-filter unsuitable
# Sequence-Aware
- Actions grouped into sessions
- NN, associated, embeddings learned form sessions.
### Converstational
### Casual Inference
- Observational: predict y given x.
- Interventional Predict user rating given we recommended that item, use in future to tune.
