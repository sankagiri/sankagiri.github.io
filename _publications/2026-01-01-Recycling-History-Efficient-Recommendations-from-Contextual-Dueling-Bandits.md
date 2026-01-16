---
title: "Recycling History: Efficient Recommendations from Contextual Dueling Bandits"
collection: publications
permalink: /publication/2026-01-01-Recycling-History-Efficient-Recommendations-from-Contextual-Dueling-Bandits
category: conferences
date: 2026-01-01
venue: 'ALT'
excerpt: ''
---
The contextual dueling bandit problem models adaptive recommender systems in which, at each step, the algorithm presents a set of items to the user and the user's choice reveals their preference. While this setup captures implicit choices made during content navigation, it does not account for other natural comparison queries. Motivated by the observation that users provide more reliable feedback after consuming items, we propose a new bandit model in which the algorithm recommends a single item at each time step and, after consumption, asks the user to compare it with another item chosen from their consumption history. Crucially, this comparison item can be selected without incurring additional regret, potentially improving performance. The regret analysis is challenging due to temporal dependencies induced by the user's history. To address this, we show that informative comparison queries can be constructed once the history is sufficiently rich, satisfying a suitable diversity condition. We then prove that a short initial random exploration phase suffices to build such a rich history with high probability. Using matrix concentration arguments, this leads to $O(\sqrt{T})$ regret guarantees. Simulations further demonstrate that reusing past items for comparisons can significantly reduce regret compared to only comparing simultaneously recommended items.
