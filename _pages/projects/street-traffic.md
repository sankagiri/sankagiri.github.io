---
layout: student-project
permalink: /projects/street-traffic/
title: "Why does the queue at your street corner grow?"
description: "Measure arrivals, departures, and queues at one permitted viewpoint, then validate a small traffic model before testing interventions."
project_fit: "You like watching how a city works and can combine observation, coding, and careful measurement."
project_resources: "A phone or camera, a stable permitted viewpoint, manual annotations, and a laptop."
project_budget: "₹0–10k with an existing camera; a GPU is optional for faster video processing."
---

Why does the queue at your street corner suddenly grow? A bus stops, a vehicle turns, or the signal changes—and a small disturbance travels through the traffic. Observe one corner closely and see whether you can explain one such pattern.

You can begin with a notebook and stopwatch. A camera and a simulator can come later.

## Try this first

From a safe, permitted viewpoint, spend a short session counting vehicles entering and leaving a clearly defined region. Note the queue length every minute. Plot all three quantities together: does the queue grow when arrivals exceed departures?

Choose what you mean by a queue. In mixed Indian traffic, ten two-wheelers and ten buses occupy very different amounts of road. Counting vehicles, people, and occupied road length answers different questions.

## Follow a question

Repeat the observation on another day. Perhaps queues depend on turning vehicles, pedestrians, or a bus stop more than on the traffic signal. Follow the pattern that interests you.

If manual counting becomes tedious, try a video detector and tracker. Compare its counts with your own, especially when vehicles overlap or remain stopped. An impressive annotated video can still count the same vehicle twice.

A simple queue model may explain what you saw. If interactions matter, [SUMO](https://sumo.dlr.de/docs/index.html) offers a route to modelling one junction. Supply measured arrivals and turning proportions where possible, then see whether the model reproduces a different observation session before asking “what if we changed the signal?”

## Keep yourself honest

- Test automated counts or predictions on a new recording session. Nearby frames are almost the same example.
- Pixels per second are not kilometres per hour. Estimating speed needs a geometric reference; useful counts do not. Do not enter traffic to place markers.
- Simulated improvements depend on assumed demand and behaviour. Compare policies under the same conditions and include effects on different road users.

Frame observations around aggregate movement. Obtain permission for the viewpoint and equipment, avoid private spaces and identifying details, and share counts or suitably obscured examples rather than a surveillance archive.

## If it gets interesting

You might explore traffic waves, queueing, network flow, or learned arrival forecasts. A clear explanation of one recurring queue is already worthwhile. Expanding to several junctions needs synchronised observations, better demand data, and cooperation from site owners or transport authorities. Changing real signals is not part of the independent starter.
