---
layout: student-project
permalink: /projects/queue-lab/
title: "Make a canteen queue less miserable"
description: "Build a discrete-event queue simulator, check it against observations, and compare service policies at equal resource cost."
project_fit: "You like probability, optimisation, and finding a mathematical question in everyday college life."
project_resources: "An ordinary laptop; optional anonymous timing observations made with permission."
project_budget: "₹0–3,000 for a notebook, simple counter, or phone stand if needed. No special instrument or GPU is required."
---

Why does one canteen queue move steadily while another suddenly becomes enormous? Would a shared queue help? What if payment happened at a separate counter, or another server opened only during the rush?

Build a small simulator and play with these possibilities without disrupting anyone's lunch. It might lead you towards probability and optimisation—or towards the discovery that the queue is not the real bottleneck.

## Try one counter first

Use [SimPy](https://simpy.readthedocs.io/en/latest/simpy_intro/basic_concepts.html), or a short Python program, to represent arrivals, service and departures. Begin with a handful of arrival times and service durations you choose yourself. Work out the waiting times on paper and compare them with the program. Draw a timeline: who is waiting, and who is being served?

Nobody should leave before arriving, and a server cannot serve two people at once. AI can help build the simulation and explain the code; your small hand-worked example is an independent check.

## Bring in a little college life

With the operator's permission, observe anonymous arrival counts, service durations and queue lengths. A mock canteen with willing friends also works. You do not need names, faces or payment details. If access is difficult, invent several patterns and be clear that they are assumptions.

Are arrivals steady, or do whole groups appear after a lecture? Does a complicated order slow everyone down? Use some observation sessions to adjust the simulator, then see whether it reproduces a session you kept aside. Look at the longest waits as well as the average. If it misses badly, investigate before asking it to recommend changes.

From there, try shared versus separate queues, an express counter, batching, or a rule for opening another counter. Compare the same rush patterns with the same total staffing time. Include switching delays, and ask whether helping one group makes another wait much longer.

## There are several ways to go deeper

An ML model could forecast arrivals or choose staffing, but compare it with something simple, such as opening a counter when the queue gets long. Do not secretly give it future arrivals or service times. Try new rush patterns, not just new random runs of the same pattern.

Perhaps the kitchen, rather than the payment counter, turns out to control everything. Add that stage if it interests you. A real trial would need permission and the operator's knowledge; a carefully checked simulation is already a worthwhile independent project. You can change direction as the observations teach you what matters.
