---
layout: student-project
permalink: /projects/solar-panel/
title: "How much sunshine can you actually use?"
description: "Measure a small solar panel through shade, clouds, and heat, then predict the power it can deliver."
project_fit: "You like outdoor experiments, circuits, and models that can be checked against measurements."
project_resources: "A small low-voltage panel, suitable loads, voltage/current logging, and access to a sunny spot."
project_budget: "₹8,000–₹20,000 for the core apparatus."
---

A leaf's shadow crosses a solar panel. How much power disappears? The answer may depend on where the shadow falls, not just its size. A small panel on a balcony can turn sunshine into a surprisingly rich experiment.

Start with a 10–20 W panel, voltage and current measurement, and suitable electrical loads—components that draw power from it. You can explore the panel directly without batteries or an inverter. See the [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) for equipment and price anchors.

## Try this first

Under reasonably steady sunlight, connect a few appropriately rated loads in turn. Measure voltage and current and multiply them to get power. Plot power against voltage: which load gets the most out of the panel?

Ask an electronics club member to check the circuit and component ratings. A panel labelled “12 V” does not supply a constant 12 V. Check your readings against a multimeter; measuring voltage with nothing connected does not tell you how much useful power is available.

Repeat a curve after changing the panel's angle. If a cloud passes halfway through, keep that observation, but mark the curve as a changing-weather experiment.

## Follow the interesting part

- **Which shadows matter?** Briefly compare different shadow positions, following the panel manufacturer's operating guidance. Can the cell arrangement explain an unexpectedly large loss?
- **Does a hot panel behave differently?** Record panel-back temperature as well as sunshine. Can you separate heating from the fact that brighter sunshine often makes the panel hotter?
- **Can you predict the next cloud's effect?** Forecast power delivered to one fixed load using recent measurements. First compare with the simple prediction that power will stay at its current value. Then consider a small neural network if the errors suggest something it could learn.

## Keep the measurements honest

A cheap light sensor gives a useful brightness proxy, not a calibrated measurement of incoming solar energy. Repeat comparisons on different days and vary their order. Otherwise “shaded” may always mean “measured later, when the sun had moved.” Test any forecasting model on whole unseen days rather than randomly selected seconds.

Further exploration leads to semiconductor physics and circuits that continually adjust the load to extract more power. A second matched panel can make comparisons fairer. More ambitious experiments need a stable outdoor site, permission to use it, good reference measurements, and electronics expertise. Buying a bigger panel will not answer those questions by itself.
