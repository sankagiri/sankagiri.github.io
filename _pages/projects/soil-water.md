---
layout: student-project
permalink: /projects/soil-water/
title: "Where does the water in a flowerpot go?"
description: "Measure pot mass, soil sensor readings, drainage, and drying to build and test a small water-balance model."
project_fit: "You like plants, patient experiments, and discovering what a sensor actually measures."
project_resources: "Several identical pots, a balance, soil, capacitive probes, a logger, and a sheltered place."
project_budget: "₹5–15k for a small setup, excluding an existing laptop; spend on repeatability before automation."
---

Water two flowerpots and watch them dry. Can a ₹100 soil probe tell you how much water remains? What if moving it a centimetre changes the answer? That small puzzle opens up a whole world of water moving through soil.

Start with unplanted pots so the first experiment is easier to interpret. You can add plants once you understand what the soil and instrument are doing.

## Try this first

Fill similar pots with the same amount of one soil mixture. Add measured water, collect the drainage, and weigh the pots as they dry. Keep a moisture probe at a marked depth and compare its readings with changes in pot mass.

Plot both curves. Does the probe follow drying smoothly, or stay nearly unchanged before dropping? Reweigh a stable object occasionally to check the balance. The [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) covers affordable equipment; borrowing a good balance can be especially useful.

## Follow the interesting part

- **What is the probe actually sensing?** Try a different insertion position or packing density. Can its reading change while the total water stays the same?
- **What slows drying?** Compare mulch, exposed soil area, or airflow. Swap pot positions and repeat: a sunny corner can masquerade as a treatment effect.
- **Can you predict tomorrow's water loss?** Start with today's loss as your prediction. Then ask whether temperature, probe readings, or a simple learned model add useful information.

There is plenty to investigate before building an automatic watering system. A result showing that weighing works better than the probe would be interesting in its own right.

## Keep the measurements honest

The [DFRobot probe guide](https://wiki.dfrobot.com/sen0193) offers a useful starting example, but its air/water demonstration does not calibrate water content in your soil. Compare each probe against measured changes in water mass. A reading labelled “moisture” does not measure plant nutrients.

Air-dried soil still contains water, so changes relative to its mass are not an absolute water-content measurement. Once plants enter the experiment, growth and plant water use complicate the balance too.

If you build a model, test it on whole unseen pots or watering–drying cycles, not shuffled readings from the same cycle. Further questions lead to flow through porous materials and why wetting and drying can follow different paths. Taking this to a farm would need land access, reference soil measurements, agronomic advice, and patience across growing cycles.
