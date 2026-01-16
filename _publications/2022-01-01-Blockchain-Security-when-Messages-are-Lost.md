---
title: "Blockchain Security when Messages are Lost"
collection: publications
permalink: /publication/2022-01-01-Blockchain-Security-when-Messages-are-Lost
category: workshops
date: 2022-01-01
venue: 'ConsensusDay@CCS'
---
Security analyses for consensus protocols in blockchain research have primarily focused on the synchronous model, where point-to-point communication delays are upper bounded by a known finite constant. These models are unrealistic in noisy settings, where messages may be lost (i.e. incur infinite delay). In this work, we study the impact of message losses on the security of the proof-of-work longest-chain protocol. We introduce a new communication model to capture the impact of message loss called the $0-\\infty$ model, and derive a region of tolerable adversarial power under which the consensus protocol is secure. The guarantees are derived as a simple bound for the probability that a transaction violates desired security properties. Specifically, we show that this violation probability decays almost exponentially in the security parameter. Our approach involves constructing combinatorial objects from blocktrees, and identifying random variables associated with them that are amenable to analysis. This approach improves existing bounds and extends the known regime for tolerable adversarial threshold in settings where messages may be lost.
