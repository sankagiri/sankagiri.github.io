---
title: "Blockchain CAP Theorem Allows User-Dependent Adaptivity and Finality"
authors: '<b>Suryanarayana Sankagiri</b>, Xuechao Wang, Sreeram Kannan, Pramod Viswanath'
collection: publications

permalink: /publication/2021-01-01-Blockchain-CAP-Theorem-Allows-User-Dependent-Adaptivity-and-Finality
category: conferences
date: 2021-01-01
venue: 'Financial Cryptography (2)'
excerpt: ''
---
Longest-chain blockchain protocols, such as Bitcoin, guarantee liveness even when the number of actively participating users is variable, i.e., they are adaptive. However, they are not safe under network partitions, i.e., they do not guarantee finality. On the other hand, classical blockchain protocols, like PBFT, achieve finality but not adaptivity. Indeed, the CAP theorem in the context of blockchains asserts that no protocol can simultaneously offer both adaptivity and finality. We propose a new blockchain protocol, called the checkpointed longest chain, that offers individual users the choice between finality and adaptivity instead of imposing it at a system-wide level. This protocol's salient feature is that it supports two distinct confirmation rules: one that guarantees adaptivity and the other finality. The more optimistic adaptive rule always confirms blocks that are marked as finalized by the more conservative rule, and may possibly confirm more blocks during variable participation levels. Clients (users) make a local choice between the confirmation rules as per their personal preference, while miners follow a fixed block proposal rule that is consistent with both confirmation rules. The proposed protocol has the additional benefit of intrinsic validity: the finalized blocks always lie on a single blockchain, and therefore miners can attest to the validity of transactions while proposing blocks. Our protocol builds on the notion of a finality gadget, a popular technique for adding finality to longest-chain protocols.
