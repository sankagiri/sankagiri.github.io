---
layout: student-project
permalink: /projects/tamil-arena/
title: "Which Tamil answer do people prefer?"
description: "Build a small Tamil answer-comparison app and compare human preferences with an AI judge while checking position effects and uncertainty."
project_fit: "You like statistics and simple web applications, and can work with fluent readers of Tamil or another chosen language."
project_resources: "Two models, cached answers, a laptop, and willing adult participants. A live GPU server is unnecessary."
---

Show someone two anonymous answers to the same Tamil question. Which do they prefer, and why? Now ask an AI judge to choose. Investigate where the judgements agree—and where people disagree with one another.

Choose a setting you care about, such as explaining science in everyday Tamil. Another language you know well works too.

## Try this first

Write a few prompts and save answers from two models. Put the answers side by side on a simple page without model names. Cached answers are enough; you do not need a live GPU server.

Offer choices for either answer, a tie, both poor, and cannot judge. Randomise which answer appears on the left. Use dummy votes to check that swapping the display does not accidentally swap the stored winner.

Ask a few willing fluent adult readers to try it. Explain what you record and how you intend to use it; avoid names and personal prompts. Keep public sharing within the permission participants gave.

## Follow a question

Do people value natural phrasing more than detail? Does a fluent but incorrect answer win? Does mixing Tamil and English change preferences? Pick one question rather than building a general leaderboard.

Have several people judge some of the same pairs, and invite a short explanation. Start with vote counts. Fifty votes from five friends are still observations from five people, not fifty independent readers.

Give an AI judge the same saved pairs in both orders. Compare its choices with the human votes and inspect order-dependent verdicts. If you change the judge's instructions after seeing these results, use fresh prompts and votes to check the change.

## Keep yourself honest

- A fluent reader should check language quality; factual questions also need someone who understands the topic.
- Preserve ties and “both poor” responses. Quietly discarding them can create a misleading winner.
- Longer answers may be more useful. A link between length and preference does not alone prove bias.
- Your conclusions describe these prompts and readers. A small group cannot establish the best model for all Tamil speakers.

## If it gets interesting

Explore one disagreement in depth, add another language, or compare more models. Statistical ranking methods become useful when you have enough comparisons; they need not be your first task.

[Chatbot Arena](https://arxiv.org/abs/2403.04132) explains large-scale pairwise evaluation, and [Judging the Judges](https://arxiv.org/abs/2406.07791) studies position effects. A small app and a thoughtful account of where agreement breaks down can be more interesting than a confident-looking ranking.
