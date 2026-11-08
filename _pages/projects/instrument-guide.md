---
layout: single
permalink: /projects/instrument-guide/
title: "Buying instruments for a small project"
description: "Practical Indian price anchors, numerical data access, and ways to spend on measurement rather than unnecessary hardware."
author_profile: true
---

[← All projects]({{ '/projects/' | relative_url }}) · [Working guide]({{ '/projects/working-guide/' | relative_url }})

You can do serious experimental work with a modest instrument and a carefully chosen question. Start by borrowing equipment or making one manual measurement. Buy the next item when you know which uncertainty it will resolve.

**Prices below were checked on 7 November 2026.** They are observed Indian retail listings, not supplier endorsements or quotations. Stock, shipping, taxes, bundled accessories, and quality vary. A bare sensor is usually only one part of a usable apparatus. Project budgets are planning estimates and assume access to an existing laptop and phone; they are not sums of guaranteed purchase prices.

## Some concrete price anchors

| Instrument or component | Observed listing | What the price does and does not buy |
|---|---:|---|
| [Waveshare MLX90640 55° module, Hubtronics](https://hubtronics.in/wvshare/mlx90640-d55-thermal-camera) | ₹6,499 including GST; out of stock when checked | A 32 × 24 thermal module. Add a controller, power, mounting, and reference temperature measurements. |
| [Waveshare phone thermal camera C, Robu category listing](https://robu.in/product-category/thermal-cameras/) | ₹18,629 listed | A 160 × 120 camera accessory; confirm phone compatibility and numerical export. Other phone cameras appeared from about ₹14,799. |
| [Plantower PMS5003, DNA Technology](https://www.dnatechindia.com/pms5003-pm2.5-air-quality-sensor-buy-in-india.html) | ₹1,786.23 including GST | Particle module, not a complete portable air monitor or calibrated reference instrument. |
| [SCD40 breakout, DNA Technology](https://www.dnatechindia.com/sensirion-scd40-co2-sensor-module.html) | ₹1,864.40 including GST | CO₂ module with digital output; add logging and a suitable enclosure. Verify the board and its sensor provenance. |
| [20 W, 12 V solar panel, Robu category listing](https://robu.in/product-category/solar-panel-and-controller/) | ₹1,762 listed | Panel only. Loads, current/voltage logging, connectors, and a stand cost extra. |
| [Generic capacitive soil probe, Kitkraft](https://www.kitkraft.in/products/capacitive-soil-moisture-sensor-v2-0) | ₹99 including GST | An analogue board; neither waterproofing nor a reliable percentage of soil water follows from the price. |
| [DFRobot SEN0451 industrial conductivity kit, MG Super Labs](https://www.mgsuperlabs.co.in/estore/Gravity-Analog-Electrical-Conductivity-Sensor-PRO-K1) | ₹19,709 including GST; backorder | Probe, interface, temperature sensing, and calibration accessories; a controller and experimental plumbing remain extra. |
| [HC-SR04 rangefinder, DNA Technology](https://www.dnatechindia.com/Ultrasonic-sensor-with-PWM-output.html?limit=75&order=ASC&page=5&sort=p.model) | ₹94.16 including GST | One ultrasonic distance module. A scanning rig also needs mechanics, control, and ground-truth measurements. |

## Buy access to measurements

Before ordering, find an example that reads the **numbers** on a computer. For thermal imaging, ask for native per-pixel temperature arrays, timestamps, and documented export. A colourful JPEG, an upscaled image, or a phone screen recording is not equivalent. [Melexis documents the MLX90640's native array and I²C interface](https://www.melexis.com/en/product/MLX90640/Far-Infrared-Thermal-Sensor-Array); this is a straightforward route for a programmable logger.

For other sensors, check the interface, supply voltage, signal levels, sampling interval, and whether an analogue-to-digital converter is needed. “USB charging” does not imply USB data export. Download the manual before buying. Ask an electronics club to check your proposed wiring and bill of materials.

## Know what the sensor cannot tell you

- **Thermal:** surface radiation, affected by emissivity and reflections; not a view inside a table or through walls.
- **Particles:** optical estimates affected by aerosol and environmental conditions; not a regulatory monitor or a measurement of all air pollution.
- **CO₂:** choose true CO₂ sensing. An output range is not an accuracy guarantee; check [the manufacturer's specified range](https://sensirion.com/products/catalog/SCD40).
- **Soil:** a capacitive signal needs calibration in your actual soil. It does not measure nitrogen, phosphorus, or potassium.
- **Water:** conductivity tracks ionic conduction. It cannot certify potability or rule out microbes. Use appropriate calibration standards and temperature compensation; [DFRobot's conductivity guide](https://wiki.dfrobot.com/dfr0300/) illustrates why these matter.
- **Ultrasound:** a rangefinder measures echo distance with a broad beam. A servo can make a coarse surface map, not medical-style imaging or a picture inside a chair. Full waveforms require different hardware.

## Spend in stages

These are useful **planning envelopes**, not required spending targets or quotations:

| Budget | A sensible use | What should trigger the next step |
|---|---|---|
| Up to ₹10k | Phone-based flow or vibration experiments; pots and a balance; a simple scanning rig. | A repeatable first measurement and a specific limitation. |
| ₹10–25k | One complete logged thermal, particle, CO₂, or solar experiment, including references and mounting. | Several independent runs with a checked baseline. |
| ₹25–60k | Paired or multiple loggers, better calibration, a conductivity setup, or more controlled apparatus. | Evidence that a second viewpoint or reference resolves an important ambiguity. |
| ₹60k–₹1.5 lakh | A shared kit with better numerical imaging, synchronised acquisition, or several environmental stations. Obtain current quotes and test data export first. | Access to suitable sites, a clear study design, and someone able to maintain and check the equipment. |
| Above ₹1.5 lakh | Specialised acoustic imaging, reference instrumentation, or an extended field deployment. | Laboratory collaboration, domain expertise, and permissions; this is an extension rather than an independent starting requirement. |

Allow for references, calibration materials, mounting, power, storage, replacements, and repeated experiments. Two comparable instruments can reveal more than one expensive instrument: keep one fixed while moving the other, then swap them. A shared kit across a small student group is often sensible.

Check zero offsets, compare instruments side by side, document drift, and retain raw readings. Agreement between two cheap sensors is a consistency check, not traceable calibration. Keep calibration data separate from the final evaluation.

There is no requirement to spend ₹1 lakh. That level makes sense only when your question calls for better reference measurements, spatial resolution, or several synchronized instruments. At that point, laboratory access, technical advice, and permission to measure the intended system may be more valuable than another purchase.
