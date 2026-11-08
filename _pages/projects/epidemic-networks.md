---
layout: student-project
permalink: /projects/epidemic-networks/
title: "Can a small tracing team interrupt an outbreak?"
description: "Explore epidemic spread on a fictional contact network and compare intervention policies under delays, missing information, and limited resources."
project_fit: "You enjoy probability, networks, simulation, and decisions with competing costs."
project_resources: "An ordinary laptop, Python, and synthetic contacts. No personal health or location data is needed."
project_budget: "₹0 beyond an existing laptop; optional computing costs only after a small simulation works."
---

Imagine a fictional college town where a small team can investigate only a limited number of contacts each day. Should it trace household contacts first, or people who connect otherwise separate groups? How much difference does a day's delay make?

This is a way to explore networks and decisions under uncertainty. You can begin with a completely invented population; no personal health records or location histories are needed.

## Start with an outbreak you can follow

Draw a small contact network and give each person one of three states: susceptible, infectious or recovered. Write simple random rules for transmission and recovery, then plot the number in each state over time. AI can help with the code, but trace a tiny example yourself. The state counts must add up to the population, and disabling transmission must prevent new infections.

Now rearrange the contacts while keeping roughly the same number. Make households, classrooms, or a few people who bridge groups. Does the outbreak change? Run the experiment repeatedly: sometimes an outbreak dies out by chance, and one dramatic animation can be misleading.

## Follow whichever question becomes interesting

You could study the network itself, or add testing and contact tracing. Compare a simple tracing rule with random testing at the same resource budget. Introduce delays, missed contacts and people who do not follow every recommendation.

The simulated tracing team should learn about infections through its tests. Letting it inspect the hidden infection states gives it information no real team would have. Count both infections and the burden of restrictions—for example, total days people spend isolated—and look at who bears that burden.

A learned prioritisation rule could become an interesting extension. First give it a simple rule to compete against, then try it on new networks and settings. Look for conditions that reverse your original conclusion. Discovering that delay matters more than a fancy algorithm could be a strong result.

## What would make the result believable?

Keep the assumptions visible and vary uncertain ones. Matching one observed epidemic curve would not uniquely establish the contacts or behaviour that produced it. Your fictional model supports statements about its scenarios, not forecasts or restrictions for a real city.

[Covasim's overview](https://docs.covasim.org/overview.html) and [intervention tutorial](https://docs.covasim.org/tutorials/tut_interventions.html) provide a more developed example to learn from. Moving towards real public-health use requires domain expertise, suitable data and independent validation. The small network experiment already offers plenty to investigate on an ordinary laptop.
