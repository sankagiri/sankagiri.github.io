---
title: "Ranking Items from Discrete Ratings: The Cost of Unknown User Thresholds"
collection: publications
permalink: /publication/2026-01-01-Ranking-Items-from-Discrete-Ratings-The-Cost-of-Unknown-User-Thresholds
authors: 'Oscar Villemaud, <b>Suryanarayana Sankagiri</b>, Matthias Grossglauser'
date: 2026-01-01
venue: 'International Conference on Algorithmic Learning Theory (ALT)'
category: conferences
excerpt: ''
paperurl: 'https://arxiv.org/pdf/2510.01871.pdf'
---

Ranking items is a central task in many information retrieval and recommender systems, where user input often comes in the form of ratings on a coarse discrete scale. We ask whether it is possible to recover a fine-grained item ranking from such coarse-grained ratings. We model items as having scores and users as having thresholds: a user likes an item if its score exceeds their threshold and dislikes it otherwise. Although all users implicitly agree on the total item order, estimating that order is challenging when both scores and thresholds are latent. Under our model, any ranking method naturally partitions the $n$ items into ordered bins, while items within each bin remain unordered. Users arrive sequentially, and each new user can be queried to refine the current ranking. We prove that achieving a near-perfect ranking, measured by Spearman distance, requires $\Theta(n^2)$ users and therefore $\Omega(n^2)$ queries. This is significantly worse than the $O(n \log n)$ queries needed to rank from comparisons or from ratings with known user thresholds, reflecting the additional queries required to estimate each user's latent threshold. Our bound also quantifies the impact of a mismatch between the score and threshold distributions through a quadratic divergence factor. To demonstrate tightness, we provide a ranking algorithm whose query complexity matches our bound up to a logarithmic factor. Overall, our results reveal a fundamental tension in online ranking: diversity in user thresholds is necessary to aggregate coarse ratings into a fine-grained ranking, but this diversity comes at a cost when thresholds are a priori unknown.

[Download PDF](https://arxiv.org/pdf/2510.01871.pdf){: .btn .btn--info} 