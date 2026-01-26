---
title: "Merkle Trees Optimized for Stateless Clients in Bitcoin"
authors: 'Bolton Bailey, <b>Suryanarayana Sankagiri</b>'
collection: publications

permalink: /publication/2021-01-01-Merkle-Trees-Optimized-for-Stateless-Clients-in-Bitcoin
category: workshops
date: 2021-01-01
venue: 'Financial Cryptography Workshops'
excerpt: ''
---
The ever-growing size of the Bitcoin UTXO state is a factor preventing nodes with limited storage capacity from validating transactions. Cryptographic accumulators, such as Merkle trees, offer a viable solution to the problem. Full nodes create a Merkle tree from the UTXO set, while stateless nodes merely store the root of the Merkle tree. When provided with a proof, stateless nodes can verify that a transaction's inputs belong to the UTXO set. In this work, we present a systematic study of Merkle tree based accumulators, with a focus on factors that reduce the proof size. Based on the observation that UTXOs typically have a short lifetime, we propose that recent UTXOs be co-located in the tree. When proofs for different transactions are batched, such a design reduces the per-transaction proof size. We provide details of our implementation of this idea, describing certain optimizations that further reduce the proof size in practice. On Bitcoin data before August 2019, we show that our design achieves a 4.6x reduction in proof size vis-a-vis UTREEXO, which is a different Merkle-tree based system designed to support stateless nodes.
