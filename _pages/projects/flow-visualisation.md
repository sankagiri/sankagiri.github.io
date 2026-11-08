---
layout: student-project
permalink: /projects/flow-visualisation/
title: "Make flow visible"
description: "Film and analyse a tabletop dye plume or shallow water flow, distinguishing pattern motion from a measured fluid velocity field."
project_fit: "You enjoy photography, fluid mechanics, and building an experiment from everyday materials."
project_resources: "A phone with video, a fixed mount, a transparent tank or shallow tray, lighting, and small household tracers."
project_budget: "Start with household materials and an existing phone; allow ₹3–12k if building controlled flow apparatus."
---

Drop a little food colouring into water and watch it curl, spread, and sink. Change the release height or put an obstacle in its path. Can you explain what changed—and predict something about the next attempt?

This is a good project if you like making things and taking videos. The first useful experiment needs little more than a phone, a transparent container, a dropper, and steady lighting.

## Try this first

Fix your phone in place, put a ruler beside the container, and film three similar dye releases. Keep the water depth, temperature, and amount of dye roughly constant. Compare how the plume's centre and width change over time. An AI assistant can help extract frames and draw these measurements on the video.

Before adding a model, ask whether your repeated attempts look similar enough to compare. Improving the release method may become the most interesting part of the first week.

## Follow a question

What happens when the water is warmer? When a gentle current carries the dye past an obstacle? You could build a shallow tray with a small low-voltage pump, or concentrate entirely on understanding the plume in still water.

Start by tracking a few visible features. Later, compare a simple prediction—such as continuing the current motion—with a small neural network. Test on a new recording, not neighbouring frames from the video used to build the model.

## Keep yourself honest

- Lock exposure and focus where possible. Changing lighting can look like changing dye concentration.
- Dye can change water density. It may not follow the flow without affecting it.
- [Optical flow](https://docs.opencv.org/4.x/d4/dee/tutorial_optical_flow.html) measures apparent motion in an image. It is not automatically the water's velocity, especially in a three-dimensional plume.

Tracking suitable particles in shallow water is another direction; [this explanation of particle image velocimetry](https://www.dantecdynamics.com/solutions/fluid-mechanics/particle-image-velocimetry-piv/measurement-principles-of-piv/) shows what more precise measurements require. Ordinary diffuse lighting is enough to begin; laboratory lasers are unnecessary.

## What about agarbatti smoke?

It can make an interesting extension in a suitable ventilated place, with permission. Use a single small source; do not fill an enclosed room or disable alarms. Rising smoke involves buoyancy and air currents as well as diffusion. A video can reveal projected plume patterns, but cannot by itself establish pollutant concentration or three-dimensional airflow.

Let an unexpected swirl or a failed measurement lead you towards convection, mixing, or a better experiment. You do not have to turn it into a forecasting competition.
