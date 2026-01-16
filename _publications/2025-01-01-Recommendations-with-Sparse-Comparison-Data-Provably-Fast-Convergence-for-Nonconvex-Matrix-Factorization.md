---
title: "Recommendations with Sparse Comparison Data: Provably Fast Convergence for Nonconvex Matrix Factorization"
collection: publications
permalink: /publication/2025-01-01-Recommendations-with-Sparse-Comparison-Data-Provably-Fast-Convergence-for-Nonconvex-Matrix-Factorization
category: conferences
date: 2025-01-01
venue: 'ICML'
excerpt: ''
---
We consider a recommender system that elicits user feedback through pairwise comparisons rather than ratings. We study the problem of learning personalised preferences from such comparison data via collaborative filtering. Similar to the classical matrix completion setting, we assume that users and items are endowed with low-dimensional latent features, which give rise to user--item utilities. Comparison outcomes are governed by a discrete choice model over these utilities, and learning the latent features is formulated as a maximum likelihood problem over the comparison dataset. Despite the resulting optimization problem being nonconvex, we show that gradient-based methods converge exponentially to the true latent features given a warm start. Importantly, this guarantee holds in a sparse data regime, where each user compares only a small number of item pairs. Our main technical contribution is to extend key concentration results commonly used in matrix completion to this setting. Simulations show that the empirical performance exceeds theoretical predictions, even when some assumptions are relaxed. Overall, our results demonstrate that learning personalised recommendations from comparison data is both computationally and statistically efficient.
