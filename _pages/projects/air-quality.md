---
layout: student-project
permalink: /projects/air-quality/
title: "Map the air along your daily walk"
description: "Build a portable particle logger and discover which apparent pollution patterns survive repeated measurements."
project_fit: "You like fieldwork, maps, messy data, and asking whether a pattern is real."
project_resources: "An optical particle sensor, temperature/humidity logging, a phone, and repeated access to a walkable route."
project_budget: "₹8,000–₹20,000; paired instruments are a useful later upgrade."
---

Does the air change between your gate, the bus stop, and a quiet side street? Carry a particle sensor along your daily walk and you may see a striking pattern. Walk back the other way: does the pattern stay in the same place?

That second walk is where this starts becoming an investigation.

## Try this first

Build or borrow a portable particle logger, then take it along a short familiar route. Use your phone for location and note the weather and anything unusual. Pause at a few recognisable spots. Plot the readings along the walk before trying to make a polished map.

A [PMS5003](https://www.aqmd.gov/docs/default-source/aq-spec/resources-page/plantower-pms5003-manual_v2-3.pdf) uses scattered laser light to estimate particle concentration and provides numerical readings you can record. Add temperature and humidity sensing if possible. The [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) covers prices and the extra parts needed for a complete logger.

First let the instrument run in one place, follow its warm-up instructions, and check that its clock agrees with your phone. Keep its inlet clear. Its response may lag behind your movement, so a reading and a GPS dot do not necessarily describe precisely the same spot.

## Follow the interesting part

- **Is that hotspot really a place?** Repeat the route in different directions and at different times. A peak at the end of every walk might reflect changing conditions rather than a polluted corner.
- **What does the sensor respond to?** Compare dry and humid days, or run two instruments side by side. Does an apparent pattern survive those comparisons?
- **Can you predict a future walk?** Compare typical readings by location and time of day. If you try a learned model, ask whether it improves on those simple summaries.

## Keep the measurements honest

Test models on complete unseen walks or days. Adjacent seconds are too similar to provide an independent test. Show variation between visits; one dramatic reading does not establish a persistent hotspot.

Optical sensors respond differently to humidity and particle composition. They do not identify every pollutant or establish personal health risk. The [EPA Air Sensor Guidebook](https://www.epa.gov/air-sensor-toolbox/how-use-air-sensors-air-sensor-guidebook) explains these limitations and reference comparisons.

A borrowed second logger, left stationary while you walk, can help separate place from time. A larger study leads into atmospheric transport and spatial statistics, but also needs collaborators, reference instruments, and permission for fixed installations. Finding why an attractive map was misleading can be the most interesting result.
