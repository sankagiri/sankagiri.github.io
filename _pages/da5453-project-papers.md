---
title: "DA5453: Suggested Papers for the Capstone Project"
layout: single
permalink: /teaching/2026-da5453/papers/
author_profile: true
---

[Back to the course webpage](/teaching/2026-da5453)

This is a broad catalogue of papers related to the course. You are **not**
expected to read all of them. For the capstone project, each pair of students
will normally select one paper, understand its main ideas and results, present
it to the class, and carry out a computational study based on it. A project
centred on a theoretical paper must still contain an implementation of an
estimator or algorithm, at least on synthetic data.

The labels below are meant to help you begin:

- **Highly recommended** papers are particularly close to the course and lend
  themselves to a well-scoped project.
- **Recommended** papers are also strong project choices.
- *Companion reading* is useful in support of another paper, but is usually too
  broad, too specialised, or not sufficiently self-contained for a project by
  itself.

Unmarked papers are also possible choices, but their scope should be discussed
with the instructor. You may propose a paper outside this list, subject to
approval. In all cases, the precise project scope will be fixed separately.

*Last updated: 25 July 2026.*

## 1. Estimation and ranking from comparisons

- **[Rank Centrality: Ranking from Pairwise Comparisons](https://arxiv.org/abs/1209.1688)**  
  Sahand Negahban, Sewoong Oh and Devavrat Shah. *Operations Research, 2017.*  
  **Highly recommended.** The spectral algorithm and its guarantee are covered
  in class, so a project should go beyond the lecture treatment: study how the
  error depends on the topology of the comparison graph, comparing Erdős–Rényi,
  regular and poorly connected designs against BTL maximum likelihood.

- **[Fast and Accurate Inference of Plackett–Luce Models](https://papers.nips.cc/paper_files/paper/2015/hash/2a38a4a9316c49e5a833517c45d31070-Abstract.html)**  
  Lucas Maystre and Matthias Grossglauser. *NeurIPS, 2015.*  
  **Highly recommended.** The paper extends the spectral viewpoint from
  pairwise comparisons to Plackett–Luce data and develops LSR and iterative
  LSR. A suitable project can implement these algorithms and compare their
  accuracy and convergence with Rank Centrality and likelihood-based methods.

- **[Simple, Robust and Optimal Ranking from Pairwise Comparisons](https://arxiv.org/abs/1512.08949)**  
  Nihar B. Shah and Martin J. Wainwright. *JMLR, 2018.*  
  **Recommended.** This paper gives a particularly clean example in which a
  simple Borda-type procedure is both robust to model misspecification and
  statistically optimal. One can compare Borda, BTL maximum likelihood and
  Rank Centrality under several synthetic comparison models.

- **[Stochastically Transitive Models for Pairwise Comparisons: Statistical and Computational Issues](https://proceedings.mlr.press/v48/shahb16.html)**  
  Nihar B. Shah, Sivaraman Balakrishnan, Adityanand Guntuboyina and Martin J.
  Wainwright. *ICML, 2016; IEEE Transactions on Information Theory, 2017.*  
  **Recommended.** The paper replaces the parametric BTL assumption by
  stochastic transitivity and studies the resulting statistical–computational
  trade-off. A project can implement the tractable estimators and examine when
  their additional flexibility is useful.

- **[Efficient Computation of Rankings from Pairwise Comparisons](https://www.jmlr.org/papers/v24/22-1086.html)**  
  M. E. J. Newman. *JMLR, 2023.*  
  **Recommended.** The proposed rearrangement of the classical Zermelo
  iteration is simple to implement and can be much faster. This makes possible
  a focused project on convergence, numerical stability and running-time
  comparisons.

- **[Accelerated Spectral Ranking](https://proceedings.mlr.press/v80/agarwal18b.html)**  
  Arpit Agarwal, Prathamesh Patil and Shivani Agarwal. *ICML, 2018.*

- **[Estimation from Pairwise Comparisons: Sharp Minimax Bounds with Topology Dependence](https://arxiv.org/abs/1505.01462)**  
  Nihar B. Shah, Sivaraman Balakrishnan, Joseph Bradley, Abhay Parekh, Kannan
  Ramchandran and Martin J. Wainwright. *JMLR, 2016.*

- **[A Statistical Convergence Perspective of Algorithms for Rank Aggregation from Pairwise Data](https://proceedings.mlr.press/v32/rajkumar14.html)**  
  Arun Rajkumar and Shivani Agarwal. *ICML, 2014.*

## 2. Beyond BTL and MNL: heterogeneity, context and intransitivity

- **[Learning a Mixture of Two Multinomial Logits](https://proceedings.mlr.press/v80/chierichetti18a.html)**  
  Flavio Chierichetti, Ravi Kumar and Andrew Tomkins. *ICML, 2018.*  
  **Recommended.** Mixtures provide a natural way to represent heterogeneous
  populations while retaining a clear probabilistic model. The learning
  algorithm can be implemented and tested on synthetic mixtures, including
  regimes in which a single MNL model fails.

- **[Pairwise Choice Markov Chains](https://arxiv.org/abs/1603.02740)**  
  Stephen Ragain and Johan Ugander. *NeurIPS, 2016.*  
  **Recommended.** PCMC replaces the fixed MNL weights by a Markov-chain model
  of choice and thereby permits several violations of IIA. A project can fit
  MNL and PCMC models to the same data and study predictive fit, regularity and
  computation.

- **[Modeling Intransitivity in Matchup and Comparison Data](https://www.cs.cornell.edu/~tj/publications/chen_joachims_16a.pdf)**  
  Shuo Chen and Thorsten Joachims. *WSDM, 2016.*  
  **Recommended.** The blade–chest model represents cyclic effects that a
  one-dimensional utility cannot capture. It supports a concrete project using
  synthetic rock–paper–scissors structures and one of the public matchup
  datasets studied in the paper.

- **[Discovering Context Effects from Raw Choice Data](https://arxiv.org/abs/1902.03266)**  
  Arjun Seshadri, Alexander Peysakhovich and Johan Ugander. *ICML, 2019.*  
  **Highly recommended.** The context-dependent random-utility model is a
  direct and elegant extension of the MNL model studied in Module 1. A project
  can implement its likelihood, compare it with MNL, and investigate which
  context effects can be recovered from finite data.

- **[Learning Interpretable Feature Context Effects in Discrete Choice](https://arxiv.org/abs/2009.03417)**  
  Kiran Tomlinson and Austin R. Benson. *KDD, 2021.*  
  **Highly recommended.** The linear context logit model uses observable
  features to obtain interpretable context effects. It is a natural follow-up
  to the Module 1 discussion and admits both synthetic experiments and studies
  on the datasets used by the authors.

- **[Choice Set Confounding in Discrete Choice](https://arxiv.org/abs/2105.07959)**  
  Kiran Tomlinson, Johan Ugander and Austin R. Benson. *KDD, 2021.*  
  **Recommended.** This paper asks what happens when the set of alternatives
  offered to a user is itself preference-dependent. A project can construct a
  confounded data-generating process and compare naive estimation with the
  proposed causal corrections.

## 3. Personalised preferences, implicit feedback and learning to rank

- **[Preference Completion: Large-scale Collaborative Ranking from Pairwise Comparisons](https://arxiv.org/abs/1507.04457)**  
  Dohyung Park, Joe Neeman, Jin Zhang, Sujay Sanghavi and Inderjit S. Dhillon.
  *ICML, 2015.*  
  **Recommended.** AltSVM gives a scalable non-convex method for learning a
  low-rank user–item score matrix from pairwise preferences. It can be compared
  with BPR and ordinary matrix factorisation on MovieLens-derived comparisons.

- **[Collaboratively Learning Preferences from Ordinal Data](https://arxiv.org/abs/1506.07947)**  
  Sewoong Oh, Kiran K. Thekumparampil and Jiaming Xu. *NeurIPS, 2015.*

- **[Learning from Comparisons and Choices](https://www.jmlr.org/papers/v19/17-607.html)**  
  Sahand Negahban, Sewoong Oh, Kiran K. Thekumparampil and Jiaming Xu. *JMLR,
  2018.*  
  *Companion reading.* This is a comprehensive treatment of the low-rank
  preference-learning framework and is best used to support a more narrowly
  scoped paper.

- **[BPR: Bayesian Personalized Ranking from Implicit Feedback](https://arxiv.org/abs/1205.2618)**  
  Steffen Rendle, Christoph Freudenthaler, Zeno Gantner and Lars Schmidt-Thieme.
  *UAI, 2009.*  
  **Highly recommended.** BPR turns implicit feedback into pairwise preferences
  and optimises a smoothed ranking criterion, which makes it a clean bridge
  from the BTL likelihood to recommendation. A project can implement the
  sampler and compare it with pointwise matrix factorisation on MovieLens.

- **[Optimizing Search Engines using Clickthrough Data](https://doi.org/10.1145/775047.775067)**  
  Thorsten Joachims. *KDD, 2002.*  
  **Highly recommended.** The paper introduces the ranking SVM and the idea of
  extracting relative judgements from clicks rather than absolute labels. A
  project can implement the pairwise ranking objective on a public
  learning-to-rank dataset and examine which click-derived constraints matter.

- **[Accurately Interpreting Clickthrough Data as Implicit Feedback](https://research.google/pubs/accurately-interpreting-clickthrough-data-as-implicit-feedback/)**  
  Thorsten Joachims, Laura Granka, Bing Pan, Helene Hembrooke and Geri Gay.
  *SIGIR, 2005.*  
  **Highly recommended.** This eye-tracking study established position bias and
  motivated relative rather than absolute interpretations of clicks. Being
  empirical, it is best turned into a simulation: build a click model carrying
  the biases it documents and measure how they distort estimated relevance.

- **[Unbiased Learning-to-Rank with Biased Feedback](https://arxiv.org/abs/1608.04468)**  
  Thorsten Joachims, Adith Swaminathan and Tobias Schnabel. *WSDM, 2017.*  
  **Highly recommended.** Propensity-weighted ERM makes the debiasing of click
  data precise and yields an unbiased risk estimate for ranking. A project can
  implement the IPS estimator, vary the propensity model, and measure the bias
  and variance trade-off against a naive click-trained ranker.

- **[Position Bias Estimation for Unbiased Learning to Rank in Personal Search](https://research.google/pubs/position-bias-estimation-for-unbiased-learning-to-rank-in-personal-search/)**  
  Xuanhui Wang, Nadav Golbandi, Michael Bendersky, Donald Metzler and Marc
  Najork. *WSDM, 2018.*  
  **Recommended.** The regression-EM method estimates position propensities
  without requiring fully randomised rankings. A project can simulate a click
  model, recover the propensities and measure the downstream effect on an IPS
  learning-to-rank estimator.

- **[Recommendations as Treatments: Debiasing Learning and Evaluation](https://proceedings.mlr.press/v48/schnabel16.html)**  
  Tobias Schnabel, Adith Swaminathan, Ashudeep Singh, Navin Chandak and Thorsten
  Joachims. *ICML, 2016.*  
  **Recommended.** This is a clean bridge from inverse-propensity weighting to
  matrix factorisation. The proposed estimator can be studied on semi-synthetic
  data where exposure propensities and the true prediction risk are known.

- **[Unbiased Recommender Learning from Missing-Not-At-Random Implicit Feedback](https://arxiv.org/abs/1909.03601)**  
  Yuta Saito, Suguru Yaginuma, Yuta Nishino, Hayato Sakata and Kazuhide Nakata.
  *WSDM, 2020.*  
  **Recommended.** The paper derives unbiased and clipped estimators for
  recommendation from non-randomly missing feedback. It offers a manageable
  bias–variance study using synthetic exposure and relevance models.

## 4. Ordinal and triplet embedding

- **[Adaptively Learning the Crowd Kernel](https://arxiv.org/abs/1105.1033)**  
  Omer Tamuz, Ce Liu, Serge Belongie, Ohad Shamir and Adam Tauman Kalai. *ICML,
  2011.*  
  **Recommended.** This paper combines triplet-based similarity judgements,
  kernel learning and adaptive query selection. A project can implement the
  basic estimator and compare adaptive and random triplet collection.

- **[Stochastic Triplet Embedding](https://doi.org/10.1109/MLSP.2012.6349720)**  
  Laurens van der Maaten and Kilian Q. Weinberger. *MLSP, 2012.*  
  **Recommended.** STE and t-STE give a direct probabilistic route from
  triplet comparisons to a visual embedding. The methods are straightforward
  to implement and permit clear comparisons with standard triplet-loss
  baselines.

- **[Local Ordinal Embedding](https://proceedings.mlr.press/v32/terada14.html)**  
  Yoshikazu Terada and Ulrike von Luxburg. *ICML, 2014.*

- **[Finite Sample Prediction and Recovery Bounds for Ordinal Embedding](https://arxiv.org/abs/1606.07081)**  
  Lalit Jain, Kevin Jamieson and Robert Nowak. *NeurIPS, 2016.*  
  **Recommended.** The paper connects noisy triplets, low-rank distance
  matrices and finite-sample recovery, while also proposing projected-gradient
  algorithms. A project can reproduce its synthetic recovery experiments and
  examine the effect of dimension, noise and triplet sampling.

- **[Cost-Effective HITs for Relative Similarity Comparisons](https://ojs.aaai.org/index.php/HCOMP/article/view/13152)**  
  Michael J. Wilber, Iljung S. Kwak and Serge J. Belongie. *HCOMP, 2014.*  
  *Companion reading and dataset.*

## 5. Preference-based alignment: foundations and training objectives

- **[Deep Reinforcement Learning from Human Preferences](https://papers.nips.cc/paper/7017-deep-reinforcement-learning)**  
  Paul Christiano, Jan Leike, Tom B. Brown, Miljan Martic, Shane Legg and Dario
  Amodei. *NeurIPS, 2017.*  
  **Highly recommended.** This is the paper that placed BTL reward learning
  inside a deep RL loop, and only its main idea is covered in class. A project
  can reproduce preference-based reward learning on a small control task and
  study how the query budget and label noise affect the learnt policy.

- **[Training Language Models to Follow Instructions with Human Feedback](https://proceedings.neurips.cc/paper_files/paper/2022/hash/b1efde53be364a73914f58805a001731-Abstract.html)**  
  Long Ouyang et al. *NeurIPS, 2022.*  
  **Highly recommended.** InstructGPT is the reference description of the full
  three-stage RLHF pipeline. A project must necessarily work at small scale:
  fit a reward model on a public preference dataset and examine how its
  accuracy and calibration vary with data size and annotator disagreement.

- **[Direct Preference Optimization: Your Language Model is Secretly a Reward Model](https://proceedings.neurips.cc/paper_files/paper/2023/hash/a85b405ed65c6477a4fe8302b5e06ce7-Abstract-Conference.html)**  
  Rafael Rafailov, Archit Sharma, Eric Mitchell, Christopher D. Manning, Stefano
  Ermon and Chelsea Finn. *NeurIPS, 2023.*  
  **Highly recommended.** The reparameterisation that removes the explicit
  reward model is short enough to be worked through in full detail. A project
  can implement DPO on a small model or a bandit surrogate, and test where its
  claimed equivalence with RLHF breaks down in practice.

- **[Principled Reinforcement Learning with Human Feedback from Pairwise or K-wise Comparisons](https://arxiv.org/abs/2301.11270)**  
  Banghua Zhu, Michael I. Jordan and Jiantao Jiao. *ICML, 2023.*  
  **Recommended.** The paper joins the BTL/Plackett–Luce estimation problem to
  offline policy optimisation through pessimism. Its key ideas can be studied
  in a finite-action simulator without training a large language model.

- **[A General Theoretical Paradigm to Understand Learning from Human Preferences](https://arxiv.org/abs/2310.12036)**  
  Mohammad Gheshlaghi Azar et al. *AISTATS, 2024.*  
  **Highly recommended.** The paper places RLHF, DPO and related objectives in
  a common framework and motivates Identity Preference Optimisation (IPO). A
  project can derive and implement the objectives in a tabular or small-model
  setting and compare their behaviour under noisy preferences.

- **[Model Alignment as Prospect Theoretic Optimization](https://arxiv.org/abs/2402.01306)**  
  Kawin Ethayarajh, Winnie Xu, Niklas Muennighoff, Dan Jurafsky and Douwe Kiela.
  *ICML, 2024.*  
  **Recommended.** KTO replaces paired comparisons by desirable and
  undesirable examples and connects the objective to prospect theory. A
  scaled-down project can compare KTO and DPO under controlled pairing and
  label-noise conditions.

- **[Provably Robust DPO: Aligning Language Models with Noisy Feedback](https://arxiv.org/abs/2403.00409)**  
  Sayak Ray Chowdhury, Anush Kini and Nagarajan Natarajan. *ICML, 2024.*  
  **Recommended.** The proposed correction gives a precise way to study random
  preference-label flips. It can be implemented with a small policy model and
  evaluated while varying the noise rate and its misspecification.

- **[SimPO: Simple Preference Optimization with a Reference-Free Reward](https://arxiv.org/abs/2405.14734)**  
  Yu Meng, Mengzhou Xia and Danqi Chen. *NeurIPS, 2024.*

## 6. Alignment diagnostics, data, inference and personalisation

- **[Unintentional Unalignment: Likelihood Displacement in Direct Preference Optimization](https://arxiv.org/abs/2410.08847)**  
  Noam Razin, Sadhika Malladi, Adithya Bhaskar, Danqi Chen, Sanjeev Arora and
  Boris Hanin. *ICLR, 2025.*  
  **Highly recommended.** The paper isolates a surprising training-dynamics
  failure of DPO and provides code and diagnostics. This supports a
  compute-conscious project based on reproducing likelihood displacement and
  testing the proposed CHES score. ([Code](https://github.com/princeton-nlp/unintentional-unalignment))

- **[Preference Learning Algorithms Do Not Learn Preference Rankings](https://arxiv.org/abs/2405.19534)**  
  Angelica Chen et al. *NeurIPS, 2024.*  
  **Recommended.** The paper separates pairwise training accuracy from recovery
  of an entire preference ranking. Much of the project can be inference-only:
  evaluate several learned or synthetic reward functions under ordinary and
  ranking-aware metrics.

- **[Theoretical Guarantees on the Best-of-n Alignment Policy](https://arxiv.org/abs/2401.01879)**  
  Ahmad Beirami et al. *ICML, 2025.*

- **[Scaling Laws for Reward Model Overoptimization](https://arxiv.org/abs/2210.10760)**  
  Leo Gao, John Schulman and Jacob Hilton. *ICML, 2023.*  
  **Recommended.** The paper gives an empirical account of Goodhart-like
  behaviour when a proxy reward is optimised too strongly. A scaled-down
  project can reproduce the phenomenon with synthetic gold and proxy reward
  models.

- **[FisherSFT: Data-Efficient Supervised Fine-Tuning of Language Models Using Information Gain](https://arxiv.org/abs/2505.14826)**  
  Rohan Deb et al. *ICML, 2025.*

- **[LoRe: Personalizing LLMs via Low-Rank Reward Modeling](https://arxiv.org/abs/2504.14439)**  
  Avinandan Bose, Zhihan Xiong, Yuejie Chi, Simon S. Du, Lin Xiao and Maryam
  Fazel. *COLM, 2025.*  
  **Recommended.** LoRe treats variation across users as low-rank structure in
  the reward matrix, making a useful bridge to collaborative preference
  learning. Its frozen-embedding implementation permits experiments without
  full LLM fine-tuning. ([Code](https://github.com/facebookresearch/LoRe))

- **[Language Model Personalization via Reward Factorization](https://arxiv.org/abs/2503.06358)**  
  Idan Shenfeld, Felix Faltings, Pulkit Agrawal and Aldo Pacchiano. *COLM,
  2025.*  
  *Companion reading for a project on low-rank personalised rewards.*

- **[Distributional Preference Learning: Understanding and Accounting for Hidden Context in RLHF](https://arxiv.org/abs/2312.08358)**  
  Anand Siththaranjan, Cassidy Laidlaw and Dylan Hadfield-Menell. *ICLR, 2024.*  
  **Recommended.** The paper treats annotator disagreement as information about
  hidden context rather than as independent noise. A project can construct a
  heterogeneous annotator population and compare scalar aggregation with the
  proposed distributional model.

- **[RewardBench: Evaluating Reward Models for Language Modeling](https://arxiv.org/abs/2403.13787)**  
  Nathan Lambert et al. *Findings of NAACL, 2025.*  
  **Highly recommended.** RewardBench turns reward-model evaluation into a
  modular and reproducible problem covering chat, reasoning and safety. A
  project can evaluate small open reward models, add a controlled stress-test
  subset, and analyse failure patterns. ([Code](https://github.com/allenai/reward-bench))

- **[AlpacaFarm: A Simulation Framework for Methods that Learn from Human Feedback](https://papers.nips.cc/paper_files/paper/2023/hash/5fc47800ee5b30b8777fdd30abcaaf3b-Abstract-Conference.html)**  
  Yann Dubois et al. *NeurIPS, 2023.*  
  *Companion reading and software framework.* ([Code](https://github.com/tatsu-lab/alpaca_farm))

## 7. Active ranking and dueling bandits

- **[The K-armed Dueling Bandits Problem](https://www.cs.cornell.edu/~tj/publications/yue_etal_09a.pdf)**  
  Yisong Yue, Josef Broder, Robert Kleinberg and Thorsten Joachims. *JCSS, 2012;
  conference version at COLT, 2009.*  
  **Recommended.** This foundational paper develops Interleaved Filter, which
  is not covered in detail in class. It provides a natural baseline
  implementation and a starting point for comparing later dueling-bandit
  algorithms.

- **[Relative Upper Confidence Bound for the K-Armed Dueling Bandit Problem](https://arxiv.org/abs/1312.3393)**  
  Masrour Zoghi, Shimon Whiteson, Rémi Munos and Maarten de Rijke. *ICML,
  2014.*  
  **Highly recommended.** RUCB is the natural optimistic algorithm for duels
  and requires no explicit exploration phase. A project can implement it,
  examine its regret on preference matrices with and without a Condorcet
  winner, and compare it with Interleaved Filter and Double Thompson Sampling.

- **[Regret Lower Bound and Optimal Algorithm in Dueling Bandit Problem](https://arxiv.org/abs/1506.02550)**  
  Junpei Komiyama, Junya Honda, Hisashi Kashima and Hiroshi Nakagawa. *COLT,
  2015.*

- **[Double Thompson Sampling for Dueling Bandits](https://arxiv.org/abs/1604.07101)**  
  Huasen Wu and Xin Liu. *NeurIPS, 2016.*  
  **Recommended.** Double Thompson Sampling has a simple posterior-sampling
  implementation and works for both Condorcet and Copeland settings. It can be
  compared directly with RUCB on synthetic and public preference matrices.

- **[Copeland Dueling Bandits](https://arxiv.org/abs/1506.00312)**  
  Masrour Zoghi, Zohar Karnin, Shimon Whiteson and Maarten de Rijke. *NeurIPS,
  2015.*  
  **Recommended.** This paper removes the assumption that a Condorcet winner
  exists. A project can generate cyclic preference matrices and compare
  Condorcet-based, Copeland-based and Thompson-sampling approaches.

- **[Reducing Dueling Bandits to Cardinal Bandits](https://arxiv.org/abs/1405.3396)**  
  Nir Ailon, Zohar Karnin and Thorsten Joachims. *ICML, 2014.*

- **[Active Ranking using Pairwise Comparisons](https://proceedings.neurips.cc/paper_files/paper/2011/hash/6c14da109e294d1e8155be8aa4b1ce8e-Abstract.html)**  
  Kevin G. Jamieson and Robert Nowak. *NeurIPS, 2011.*  
  **Recommended.** The paper exploits a low-dimensional geometric structure to
  select informative comparisons. A project can implement the noiseless and
  robust procedures and measure the gain over random querying as the dimension
  changes.

- **[Just Sort It! A Simple and Effective Approach to Active Preference Learning](https://proceedings.mlr.press/v70/maystre17a.html)**  
  Lucas Maystre and Matthias Grossglauser. *ICML, 2017.*  
  **Highly recommended.** The central idea—repeated noisy sorting—is simple,
  surprising and very easy to implement, while still admitting useful theory.
  A project can compare repeated Quicksort with random sampling and more
  elaborate active-ranking rules under BTL and misspecified models.

- **[Active Ranking from Pairwise Comparisons and When Parametric Assumptions Do Not Help](https://arxiv.org/abs/1606.08842)**  
  Reinhard Heckel, Nihar B. Shah, Kannan Ramchandran and Martin J. Wainwright.
  *Annals of Statistics, 2019.*

- **[Maximum Selection and Ranking under Noisy Comparisons](https://arxiv.org/abs/1705.05366)**  
  Moein Falahatgar, Alon Orlitsky, Venkatadheeraj Pichapati and Ananda Theertha
  Suresh. *ICML, 2017.*  
  **Highly recommended.** The paper gives near-optimal sample complexities for
  maximum selection and for ranking under strong stochastic transitivity, by
  means of pleasingly simple tournament-style algorithms. A project can
  implement them and compare empirical sample counts with the stated bounds.

## 8. Contextual, multiway and assortment bandits

- **[Thompson Sampling for the MNL-Bandit](https://arxiv.org/abs/1706.00977)**  
  Shipra Agrawal, Vashist Avadhanula, Vineet Goyal and Assaf Zeevi. *COLT,
  2017.*  
  **Recommended.** This paper complements the UCB method discussed in class
  with a posterior-sampling algorithm for dynamic assortment selection. A
  project can implement both approaches and compare their regret across
  assortment sizes and parameter regimes.

- **[MNL-Bandit: A Dynamic Learning Approach to Assortment Selection](https://arxiv.org/abs/1706.03880)**  
  Shipra Agrawal, Vashist Avadhanula, Vineet Goyal and Assaf Zeevi. *Operations
  Research, 2019.*  
  **Highly recommended.** This is the journal treatment of the UCB approach to
  assortment selection discussed in class, including the matching lower bound.
  A project can implement the epoch-based algorithm, reproduce the regret
  curves and study sensitivity to assortment size and revenue parameters.

- **[Thompson Sampling for Multinomial Logit Contextual Bandits](https://papers.nips.cc/paper_files/paper/2019/hash/36d7534290610d9b7e9abed244dd2f28-Abstract.html)**  
  Min-hwan Oh and Garud Iyengar. *NeurIPS, 2019.*

- **[Contextual Dueling Bandits](https://arxiv.org/abs/1502.06362)**  
  Miroslav Dudík, Katja Hofmann, Robert E. Schapire, Aleksandrs Slivkins and
  Masrour Zoghi. *COLT, 2015.*  
  **Recommended.** The von Neumann winner provides a game-theoretic alternative
  to assuming a Condorcet winner. A project can implement the finite-policy
  version and compare the two solution concepts on contextual preference
  matrices.

- **[Optimal Algorithms for Stochastic Contextual Preference Bandits](https://proceedings.neurips.cc/paper/2021/hash/fc3cf452d3da8402bebb765225ce8c0e-Abstract.html)**  
  Aadirupa Saha. *NeurIPS, 2021.*

- **[PAC Battling Bandits in the Plackett–Luce Model](https://arxiv.org/abs/1808.04008)**  
  Aadirupa Saha and Aditya Gopalan. *ALT, 2019.*

- **[Stochastic Contextual Dueling Bandits under Linear Stochastic Transitivity Models](https://arxiv.org/abs/2202.04593)**  
  Viktor Bengs, Aadirupa Saha and Eyke Hüllermeier. *ICML, 2022.*  
  **Recommended.** CoLSTIM connects the linear/logistic viewpoint of Module 3
  with contextual duels through perturbed utility estimates. Its synthetic
  experiments can be reproduced and extended to test model misspecification.

- **[Efficient and Optimal Algorithms for Contextual Dueling Bandits under Realizability](https://proceedings.mlr.press/v167/saha22a.html)**  
  Aadirupa Saha and Akshay Krishnamurthy. *ALT, 2022.*

- **[Battle of Bandits](https://cris.technion.ac.il/en/publications/battle-of-bandits/)**  
  Aadirupa Saha and Aditya Gopalan. *UAI, 2018.*
