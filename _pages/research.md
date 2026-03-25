---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

Primary Interests
---

My primary research focus is on learning human preferences from comparison and choice data.The key insight motivating this line of work is that comparisons can be a more informative form of feedback than ratings. Two recent works of mine serve as a motivation for this interest. Firstly, in our [ICML 2025](https://arxiv.org/pdf/2502.20033) paper, we show that learning personalized preferences by seeking comparisons is as efficient as learning from ratings, both in a statistical sense (number of data points needed) and a computational sense (fast convergence of the algorithm). Secondly, our work in [ALT 2026](https://arxiv.org/pdf/2510.01871) suggests that discretisation in ratings leads to a severe loss of information, which comparisons overcome.

Currently, I am actively working on two concrete problems. One, I am interested in designing new algorithms that can efficiently collect comparisons in an online recommendation setting. Some preliminary work in this direction was published in [ALT 2026](https://arxiv.org/pdf/2508.18841). Two, I am interested in designing richer choice models that better reflect human behavior, improving over the prediction of standard models. This direction follows from previous work published in [UAI 2025](https://arxiv.org/pdf/2508.14615), which shows that existing models do not explain real comparison data well. 

More broadly, I am motivated to build next-generation AI systems that can be used for personalised education.

Other Interests
---

In the past (during my PhD), I worked on the security and efficiency of blockchain protocols. The overarching goal of my work was to design mathematically tractable, yet realistic models, such that the ensuing mathematical analysis leads to some new practical insight. For example, we developed new security guarantees for the longest-chain protocol under stochastic network conditions; this showed that blockchains are more robust to network delays than previously believed ([Stochastic Systems 2023](https://arxiv.org/pdf/2102.00973.pdf)). Another example is my work on payment channel networks, which formulates the operation of this network as a constrained utility maximization problem; this work showed for the first time that along with routing, flow-control is also important for optimal operation of such networks ([IEEE/ACM Transactions on Networking 2025](https://arxiv.org/pdf/2502.20203.pdf)). I continue to remain interested in problems in stochastic systems, network science, and decentralized control that share a similar mathematical flavor.

In the long run, I see these two threads — learning and control — coming together in the study of systems where multiple AI agents interact with humans and with each other, each operating under limited information and competing incentives. 