---
layout: student-project
permalink: /projects/ultrasound-map/
title: "Can you draw a chair with echoes?"
description: "Build a scanning ultrasonic rangefinder and investigate the geometry, missing echoes, and resolution limits of acoustic mapping."
project_fit: "You enjoy geometry, waves, electronics, and discovering why a simple measurement fails."
project_resources: "An ultrasonic range module, a manually indexed or servo scanning mount, a controller, and measured household targets."
project_budget: "₹5–15k for a basic rig; raw-waveform experiments can require ₹30–80k or more and additional electronics skill."
---

A bat finds its way with echoes. Can you draw a chair using an inexpensive ultrasonic sensor? Try a cardboard box first, then a curtain: you may discover that an object plainly visible to your eyes almost disappears from the acoustic map.

A hobby rangefinder measures echo distance. Sweeping it can map reflecting surfaces, but **it cannot show the inside of a wooden chair** or produce medical-style ultrasound images.

## Try this first

Compare the sensor's reading with a tape measure in front of a wall. Then place a board at a fixed position and tilt it. What happens to the reported distance? Try cloth and a narrow chair leg.

Mount the sensor on a turntable marked with angles; manual rotation is fine. Scan a horizontal slice of a simple scene and draw the measured points. Measure the boxes or furniture independently so you can compare the map with something more reliable than its appearance.

The [Texas Instruments ultrasonic sensing guide](https://www.ti.com/lit/an/slaa907d/slaa907d.pdf) explains how distance comes from an echo's round-trip travel time. The [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) covers equipment choices.

## Follow the interesting part

- **Which objects disappear?** Explore surface angle, material, and size. Does a missing chair leg mean the sound passed it, bounced away, or returned too weakly?
- **Does another viewpoint help?** Scan the same scene from elsewhere. Can simple geometry combine the views and reveal an ambiguity?
- **Can a model recognise an unreliable reading?** Use repeated readings and neighbouring angles to flag doubtful returns. Compare a learned model with a simple rule before asking it to reconstruct an entire scene.

## Keep the measurements honest

A missing echo is not zero distance. A reading from the wall behind a chair is not the chair's depth. The sound covers a broad region, so tiny angular steps do not create equally fine resolution.

Test a learned method on whole unseen objects or arrangements. Show original readings beside reconstructions: a network may draw plausible chair legs that the sensor never measured.

If the echoes themselves become interesting, seek hardware that records full waveforms rather than only distance. That opens questions about multiple reflection paths and combining measurements, but requires timing and electronics skills, often with laboratory help. Imaging inside materials needs different transducers, contact coupling, and reference samples. A college lab is the place to explore that next branch; the tabletop scanner already offers plenty of wave physics.
