# FAISS Theory Questions

## Q1. What is the difference between IndexFlatL2 and IndexFlatIP? When would you use each?

### IndexFlatL2
- Uses Euclidean (L2) distance.
- Finds vectors with the smallest Euclidean distance.
- Suitable when Euclidean distance is the desired similarity metric.

### IndexFlatIP
- Uses Inner Product (dot product).
- Finds vectors with the highest dot product.
- Commonly used for cosine similarity after normalizing vectors.

### When to use each?
- Use **IndexFlatL2** for Euclidean distance comparisons.
- Use **IndexFlatIP** when vectors are normalized and cosine similarity is required.

---

## Q2. Why do we normalize embeddings before adding them to FAISS when we want cosine similarity?

Cosine similarity measures the angle between two vectors rather than their magnitude.

Normalization converts every embedding into a unit vector (length = 1).

After normalization:

- Euclidean distance becomes closely related to cosine similarity.
- Inner product between normalized vectors is equal to cosine similarity.

This ensures search results are based on semantic similarity instead of vector magnitude.

---

## Q3. FAISS uses ANN (Approximate Nearest Neighbour) search. What does "approximate" mean here and why is it acceptable?

Approximate Nearest Neighbour (ANN) means the algorithm does not always return the mathematically exact nearest vectors.

Instead, it returns vectors that are extremely close while significantly reducing computation time.

Advantages:

- Much faster searching
- Lower memory usage
- Scales to millions or billions of vectors
- Small accuracy loss (often less than 1%)

This trade-off is acceptable in production systems like Retrieval-Augmented Generation (RAG), recommendation systems, and semantic search because users benefit more from fast responses than from perfectly exact nearest neighbours.