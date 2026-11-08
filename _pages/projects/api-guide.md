---
layout: single
permalink: /projects/api-guide/
title: "Experimenting with model APIs"
description: "Small, explicit budgets for Indian-language and frontier-model experiments."
author_profile: true
---

[← All projects]({{ '/projects/' | relative_url }})

An API lets your program use a remotely hosted model. You can compare a frontier model with a smaller local model or an Indian-language model without buying a GPU. The interesting question is what improves, for whom, and at what cost.

## What might a small experiment cost?

**Rates checked 8 November 2026.** These examples use standard uncached pricing, excluding taxes, currency-conversion fees, retries and extra tools. Rupee conversions below assume **₹90 per US dollar for planning**, not a live exchange rate. Recheck the linked prices and account access before paying.

For text, imagine **100 calls, each using 1,000 input tokens and 500 billed output tokens**: 100,000 input and 50,000 output tokens overall. Tokens are pieces of text, not words; Indian scripts and different models can tokenize differently.

| Model | Price per million input / output tokens | Cost of that 100-call experiment |
|---|---:|---:|
| Sarvam 105B | ₹15 / ₹60 | ₹4.50 |
| Claude Sonnet 5.5 | $2 / $10 | $0.70 ≈ ₹63 |
| Claude Opus 5.5 | $4 / $20 | $1.40 ≈ ₹126 |

Sources: [Sarvam API documentation](https://docs.sarvam.ai/api/getting-started/pricing), [Claude API pricing](https://platform.claude.com/docs/en/about-claude/pricing). Sarvam's documentation and marketing price page differed when checked; the table follows the API documentation. Confirm the dashboard rate before a run.

Other useful Sarvam pay-as-you-go examples, from the same documentation:

| Experiment | Listed rate | Usage cost |
|---|---:|---:|
| Transcribe one hour of recorded speech | ₹0.49/minute | ₹29.40 |
| Generate 10,000 characters with Bulbul v3 | ₹3/1,000 characters | ₹30 |
| Digitise 100 document pages | ₹0.50/page | ₹50 |

These are usage costs, not guaranteed minimum top-ups. They exclude your time collecting and checking data. A **₹300–₹1,000 personal experiment budget** can support several small comparisons at these workloads; it is a suggested cap, not a requirement to spend.

## Some enjoyable directions

- **Tamil answers:** compare Sarvam with a frontier model on explanations you care about. Cache answers and ask fluent readers to judge anonymously. Does paying more improve factual accuracy, naturalness, or neither?
- **Tanglish speech:** compare Sarvam transcription with local Whisper on your own consented recordings. Then try a text model to repair transcripts. Does it fix names—or invent plausible words? Keep the original audio and human transcript as the reference.
- **Question twins:** compare a local model and a frontier API on the same verified maths questions. Report cost per correct pair alongside accuracy. An expensive model can still be sensitive to wording.
- **Company reports and tenders:** compare ordinary PDF extraction with document APIs and a language model. Keep source pages beside extracted values and test on fresh documents. A useful result may be learning when to ask a person instead.

You could also add spoken replies to a small language app and investigate pronunciation or response delay. Agree on recording and external processing with participants first. Try a tiny offline batch before building a live service.

## Keep the bill and experiment understandable

Run ten examples first and inspect the actual usage returned by the API. Estimate a larger run as **input tokens × input rate + billed output tokens × output rate**. Reasoning tokens, long conversation histories, repeated judges and tool calls can substantially increase the bill. Two models answering and a third judging means three sets of charges.

Set output limits, bound retries and stop the program at your own request/token budget; dashboard alerts are not necessarily hard spending caps. Save responses so a new plot does not repeat paid calls. Keep keys on the server or in local environment variables, never in browser code or a public repository.

Record model IDs, dates, prompts, settings, failures and costs. Hosted models can change. A model's judgement is something to evaluate against human checks, not an automatic answer key. For simulators, using an API to help write code is different from calling it at every simulation step; start with local equations and controllers.
