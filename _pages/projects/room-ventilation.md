---
layout: student-project
permalink: /projects/room-ventilation/
title: "What happens when you open the window?"
description: "Use room CO₂ measurements to investigate ventilation, mixing, and simple dynamical models."
project_fit: "You enjoy experiments that connect differential equations with a room you actually use."
project_resources: "A true CO₂ sensor, a logger, and a room where you can record window and occupancy changes."
project_budget: "₹8,000–₹20,000; a second sensor is more useful than a GPU."
---

Open a window after a room has been occupied. How quickly does its air change? Would a second window help? Does a ceiling fan bring in fresh air, or mainly mix what is already there?

CO₂ from ordinary room use gives you something measurable to follow. With a small sensor, a familiar room becomes an experiment in how air moves.

## Try this first

Record CO₂ as people use a room normally and after they leave. Mark when a door or window opens, then plot the rise and fall. On another occasion, try a different window arrangement. Use ordinary occupancy; there is no need to deliberately raise CO₂ for the experiment.

Choose a sensor that measures CO₂ directly, such as the [SCD40](https://sensirion.com/products/catalog/SCD40). Some products report “equivalent CO₂” inferred from other gases, which is unsuitable here. The [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) covers equipment choices.

Place the sensor away from someone's breath, direct sunlight, and the immediate window draught. Follow its calibration instructions, including the assumptions behind automatic baseline correction. An outdoor reading should not simply be forced to a textbook value.

## Follow the interesting part

- **Which opening makes a difference?** Compare window arrangements across ordinary days. Does the effect change with wind or indoor–outdoor temperature differences?
- **Is the room well mixed?** Borrow a second sensor and compare opposite corners, checking the units side by side first. Different curves might explain why one room-wide number is misleading.
- **Can you predict the next few minutes?** In a well-mixed empty room with steady ventilation, excess CO₂ above outdoor background falls exponentially. Fit that simple curve and look for systematic failures. A small learned correction is one possible next step, not a prerequisite.

## Keep the measurements honest

Sensor response takes time. Outdoor background can change, and somebody returning adds a new CO₂ source. Note these events rather than expecting every decay to follow the same curve.

A fitted decay rate estimates air exchange only when the mixing and steady-flow assumptions are reasonable. Test any prediction on complete unseen episodes or days. CO₂ alone does not measure every airborne pollutant.

This can lead to buoyancy, wind-driven flow, and models with several connected rooms. Your measurements could also test a room simulator. Expanding to a lecture hall or automatic ventilation control needs building access, permission, outdoor reference measurements, and engineering help. First understanding why two corners behave differently is a very good place to begin.
