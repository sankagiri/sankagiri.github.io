---
layout: student-project
permalink: /projects/room-control/
title: "Teach a room when to cool itself"
description: "Build and check a thermal model of a room, then compare cooling policies under uncertain weather and occupancy."
project_fit: "You like thermodynamics, optimisation, and the idea of an AI controller that must live with physical constraints."
project_resources: "An ordinary laptop; optional indoor/outdoor temperature loggers and permission to observe a room. The core simulation needs no GPU."
project_budget: "₹0 for the simulated seed; allow roughly ₹3,000–10,000 for optional logging instruments. Planning estimate, excluding a laptop."
---

Could your room stay comfortable with less cooling if the AC anticipated the afternoon sun or your return from class? Build a small simulator and try different ways of controlling it. You may end up more interested in how a room stores heat than in the controller itself; follow that question.

## Try a tiny room first

Begin with one temperature for the whole room. Heat enters through the walls, sunlight and occupants; the AC removes some of it. Ask an AI assistant to help turn that energy balance into a short Python simulation, with the units written down. Plot what happens when cooling switches on and off. An ordinary laptop is enough.

Check a few simple cases: without other heat sources, the room should approach the outdoor temperature. More cooling should lower its temperature. Using smaller time steps should not substantially change the answer. A convincing animation does not check any of these things for you.

## Let your own room complicate the story

If you have temperature loggers, observe ordinary warming and cooling periods, noting windows, AC settings and occupancy. Compare the sensors side by side first; keep them out of direct sun and the AC's air stream. Adjust the model using some days, then try predicting a day you have kept aside.

What explains the misses? Sunlit walls? An open door? You might add a second temperature representing the walls, or discover that your measurements cannot distinguish insulation from thermal mass. That is something to understand, not conceal with a larger model.

For control, compare a fixed schedule with an ordinary thermostat. Then try a controller that plans ahead, or a small neural model that predicts temperature. Give each method the same forecasts and operating limits. Learning by trial and error in the simulator is another possible direction.

## Keep the comparison honest

Count electrical energy, uncomfortable periods and frequent switching separately. Saving energy by tolerating a hotter room is a different result from providing the same comfort more efficiently. Test new weather and occupancy patterns, and deliberately make the simulator's parameters a little wrong. Does the clever controller still help?

[BOPTEST](https://ibpsa.github.io/project1-boptest/index.html) offers more detailed building simulations when you want a stronger test. Real deployment needs occupant consent, metering and facilities expertise. Keep early experiments simulated; do not modify mains wiring or bypass the AC's protections. A result in your model is a hypothesis about the room, not a measured saving in it.
