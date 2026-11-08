---
layout: student-project
permalink: /projects/vibration-lab/
title: "Hear what changed in an object"
description: "Use sound and vibration to identify controlled changes in a small beam, exploring resonance, damping, and generalisation."
project_fit: "You enjoy mechanics, sound, and simple experiments with surprisingly rich data."
project_resources: "A ruler or small beam, a secure clamp, small removable masses, and a phone microphone or accelerometer."
project_budget: "₹2–10k with an existing phone; ₹10–30k for additional logging hardware and repeatable fixtures if needed."
---

Clamp a ruler to a table, pluck it, and listen. Change the length sticking out, or attach a small removable mass. Can you work out what changed from the sound alone?

This simple experiment opens a path to resonance, damping, and the problem of inferring an object's properties from its response.

## Try this first

Record a few gentle plucks with a phone in a fixed position. Plot the waveform and its frequency spectrum—the frequencies present in the sound. An AI assistant can help with the code; [phyphox](https://phyphox.org/) is another starting point for phone-based experiments and data export.

Look for peaks that recur across plucks. Change one thing and record again. Does the strongest peak move? Does the vibration die away sooner? First check that repeated plucks of the unchanged ruler give reasonably similar results.

## Follow a question

You could investigate overhanging length, added mass, clamp tightness, or a damping material. Choose whichever produces a puzzling effect. Record the setup and repeat conditions in a varied order, so the recording session does not accidentally become the answer.

A simple spring–mass or beam model can help explain the peaks. Use a few measured features to predict the configuration before trying a small neural network on the waveform. [SciPy's Welch method](https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.welch.html) is a useful reference for estimating a spectrum.

Try your method on a new session, then another test piece. That is a stronger test than recognising another slice of the same recording.

## Keep yourself honest

- Moving the microphone, changing the table, or tapping harder may change the signal. Check whether the model learns those differences instead.
- A phone attached to a light beam changes its mass. A microphone placed nearby avoids that particular problem.
- Check the actual sampling rate. Phone acceleration data can miss fast vibrations, while audio processing can alter amplitude.
- Similar spectra can have different causes. A shifted peak is not a unique diagnosis of a crack.

Use small test pieces rather than weakening furniture or loading structures until they fail. This experiment cannot certify structural safety.

## If it gets interesting

Try multiple sensors, controlled tapping, or a mechanical simulation. These lead towards understanding vibration modes and comparing measured behaviour with physical predictions. Another branch is listening to raindrops on a plate; estimating rainfall would then need a reference rain gauge and tests on new storms. An unexpected failure can suggest the next question just as well as a successful prediction.
