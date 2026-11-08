---
layout: student-project
permalink: /projects/thermal-cooling/
title: "Watch heat move"
description: "Turn cooling cups and warm surfaces into experiments in heat transfer, thermal imaging, and prediction."
project_fit: "You enjoy making an invisible physical process visible, then explaining it."
project_resources: "A thermal sensor, a contact thermometer, simple household apparatus, and an ordinary laptop."
project_budget: "₹10,000–₹25,000 initially; borrow a camera if possible."
---

Watch a warm cup through a thermal camera: the handle, water surface, and table tell different stories. Why does a lid help? Does a thick cup keep a drink warm, or absorb its heat? Can you predict when it will become comfortable to drink?

You can begin with a borrowed contact thermometer. The camera adds a new way of looking, not a requirement to buy everything first.

## Try this first

Put equal amounts of comfortably warm water in similar cups, cover one, and follow their temperatures as they cool. Note the starting and room temperatures. Plot the curves and see what surprises you. Try again with the arrangements swapped; a draughty corner might explain more than the lid.

With a thermal camera, keep it fixed and save numerical temperatures as well as pictures. The [MLX90640](https://www.melexis.com/en/product/MLX90640/Far-Infrared-Thermal-Sensor-Array) has only **32 × 24 actual pixels**, so start with large objects. The [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) explains equipment choices and costs.

## Follow the interesting part

- **Where does the heat go?** Compare a lid, a sleeve, or gentle airflow. Which change matters most, and does its effect depend on how hot the water is?
- **Can one temperature describe a cup?** Compare the water, wall, and handle. Their differences may explain why a simple prediction fails.
- **Can you forecast the cooling?** Start with Newton's cooling law: the temperature difference from the room shrinks exponentially. If its errors show a pattern, a small learned model could investigate that pattern.

An ordinary laptop is enough for these models. If you try machine learning, test on complete cooling runs it has never seen; neighbouring video frames make an unfairly easy test.

## Keep the measurements honest

A thermal camera measures **surfaces**, not the water throughout a cup. Shiny materials reflect surrounding heat, and enlarging an image adds no measured detail. [FLIR explains what thermal cameras can see](https://www.flir.com/en-eu/discover/home-outdoor/can-thermal-imaging-see-through-walls/). Compare a stable matte surface with a contact probe before trusting small temperature differences.

This can grow into questions about evaporation, moving air, and heat flowing through materials. Better reference probes or access to controlled airflow may eventually matter more than a sharper camera. An unexpected curve you can explain is already a worthwhile discovery.
