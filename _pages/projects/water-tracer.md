---
layout: student-project
permalink: /projects/water-tracer/
title: "Build a tiny river and follow a tracer"
description: "Use a tabletop water channel and dye or conductivity measurements to investigate transport, mixing, and residence time."
project_fit: "You like making apparatus and asking how a small change affects a whole process."
project_resources: "A tray or transparent channel, tubing, containers, a phone, and optional conductivity logging."
project_budget: "₹5–12k for an optical version; roughly ₹20–45k with a suitable logged EC probe, standards, and temperature measurement."
---

Build a tiny stream on a table and send a pulse of food colouring through it. Add a side pocket or a bend. Does the colour arrive later, spread out, or linger somewhere you did not expect?

The same questions appear in rivers, water-treatment tanks, and chemical reactors. Your version can begin with a transparent container and a phone.

## Try this first

Run water gently through a container using a gravity feed or low-voltage pump. Add a small dye pulse and film a fixed region near the outlet against steady lighting. Plot how the colour intensity changes with time.

Measure the actual flow by collecting the outlet water for a known interval. A pump setting is not a flow measurement, and a draining reservoir can change the flow during your experiment.

Before interpreting colour as concentration, film known dilutions under the same lighting and depth. Lock the phone's exposure if possible. If you cannot establish the relationship, call your measurement colour intensity; it can still reveal interesting timing.

## Follow the interesting part

- **Where does the water linger?** Add a side pocket or obstacle. Can you explain the long tail after the main colour pulse has passed?
- **Can a simple model capture the curve?** Imagine the container mixing instantly and evenly. Its prediction depends on flow and volume. Where does your video show that assumption failing?
- **Could you infer an unseen upstream event?** Try predicting when the dye was injected from the downstream curve. Different injections can produce similar curves—how would you distinguish them?

A learned model might predict arrival time or pulse width from geometry and flow. Compare it with simple physical reasoning, and test on complete unseen runs or a new flow setting. Thousands of video frames from one run are still one experiment.

## Keep the measurements honest

Reflections, bubbles, changing depth, and camera settings can all look like changing concentration. Repeat a configuration before attributing a difference to your new obstacle.

Alternatively, follow a small salt pulse with an electrical-conductivity probe. [DFRobot's guide](https://wiki.dfrobot.com/dfr0300) explains calibration and temperature compensation; the [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) explains the added cost. Conductivity does not establish drinking-water safety. A slow sensor can also make a pulse appear more spread out.

This can grow into the study of transport and mixing, or experiments with several measurement locations. Moving beyond the tabletop requires environmental expertise and permission; releasing tracers into public waterways is a different undertaking.
