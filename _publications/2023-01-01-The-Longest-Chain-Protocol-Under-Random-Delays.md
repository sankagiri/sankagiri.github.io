---
title: "The Longest-Chain Protocol Under Random Delays"
authors: '<b>Suryanarayana Sankagiri</b>, Shreyas Gandlur, Bruce E. Hajek'
collection: publications

permalink: /publication/2023-01-01-The-Longest-Chain-Protocol-Under-Random-Delays
category: journals
date: 2023-01-01
venue: 'Stochastic Systems'
excerpt: ''
---
In the field of distributed consensus and blockchains, the synchronous communication model assumes that all messages between honest parties are delayed by at most a known constant $\Delta$. Recent literature establishes that the longest-chain blockchain protocol is secure under synchronous communication. However, these security guarantees degrade with $\Delta$. In real-world networks, communication delays may occasionally be far more than their typical value. In such a scenario, the security guarantees based on the synchronous model may be overly pessimistic, because they are based on the worst-case delay. This work analyzes the longest-chain protocol under a new network model that assumes the communication delays are random, independent, and identically distributed. The model allows for delay distributions with unbounded support. The main result of this paper is a security guarantee for the longest-chain protocol operating under this model. Our security results depend on the probability that delays exceed the interblock time period, rather than on the worst-case delay. We provide simple, explicit bounds on the security-violation probability that decays exponentially with the security parameter. Under network conditions where delays are sporadically large, our results can provide better security guarantees than prior work.
