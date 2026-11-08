---
layout: student-project
permalink: /projects/gate-twins/
title: "Do models solve a question and its twin?"
description: "Evaluate small language models on GATE-style problems and carefully checked variants, distinguishing robustness from claims about memorisation."
project_fit: "You enjoy probability, linear algebra, or ML and can verify solutions in your chosen topic."
project_resources: "Python, two small text models run one at a time, and a second reader for checking some question pairs."
---

Change the numbers in a maths question. Does a language model still solve it? What if you change only the wording?

Choose a topic you understand well—probability, linear algebra, or basic ML—and investigate how stable model answers are under small changes. [Official GATE papers](https://gate2026.iitg.ac.in/download.html) provide examples, or you can write your own questions.

## Try this first

Take five text-only, single-answer multiple-choice questions. Solve them yourself, then ask one small model to answer them. Save its responses and check your scoring by hand, including cases where it gives no clear answer.

Now write a twin for each question. Change one thing, recompute the solution, and check that the options still contain exactly one correct answer. Ask a friend to check a few pairs independently.

You have an interesting starting point when you can explain one case where the answer changes—and one where it does not.

## Follow a question

Perhaps numerical changes matter more than wording. Perhaps reordering options changes the answer. Perhaps your “equivalent” twin is actually harder. Each is worth investigating; you do not need to expand to every GATE subject.

Compare a second model, or write several twins for one kind of problem. Keep the prompt and answer budget consistent. Run each question in a fresh conversation so it cannot see its twin's solution.

Count four outcomes: both versions correct, only the original correct, only the twin correct, and neither correct. Looking at those pairs often teaches more than a single accuracy score.

## Keep yourself honest

- A performance gap does **not** prove memorisation. Wording, difficulty, grading, and accidental clues can also explain it.
- AI can draft twins, but someone who understands the mathematics must verify them.
- After changing your prompt or scorer, try fresh question pairs. Keep all versions of one question together when separating development examples from final evaluation.
- Report counts, invalid responses, and individual failures. A small selected set cannot show whether a model would pass the full exam.

Link to official papers and check reuse terms before redistributing their text. Your own questions and solutions may be easier to share.

## If it gets interesting

[GSM-Symbolic](https://arxiv.org/abs/2410.05229) explores mathematical problem variations; [JEEBench](https://arxiv.org/abs/2305.15074) is an Indian-exam evaluation precedent. Read them when a question in your own experiments gives you a reason to. A small, carefully explained failure pattern is a worthwhile outcome—even if the first error you discover is your own.

**API option:** Compare a hosted model with your local or simpler approach. See [small experiment costs and ideas]({{ '/projects/api-guide/' | relative_url }}) for Sarvam speech/text APIs and frontier models.
