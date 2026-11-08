---
layout: student-project
permalink: /projects/model-detective/
title: "Can one AI investigate another?"
description: "Test whether a model can explain, predict, or repair the behaviour of a small image classifier."
project_resources: "A small trained classifier, its images and predictions, Python, and optional access to a frontier model."
project_budget: "Start locally; optionally cap API experiments at ₹300–₹1,000. Weight dumps can cost much more than short prompts."
---

You built a flower classifier. It works in one garden and fails in another. Could a second AI work out why—and predict a mistake you have not shown it yet?

Start with a classifier from the [phone-camera project]({{ '/projects/camera-naturalist/' | relative_url }}). You need not understand every detail of neural networks to investigate its behaviour. Reading or editing raw weights is an optional, more technical branch.

## Give the detective a small mystery

Make a deliberately biased training collection: photograph one kind of object mostly against one background and another kind mostly against a different background. Include examples with backgrounds exchanged in a separate test collection. First check whether your classifier actually learned the shortcut; it may not.

Show a vision-capable model a few images and the classifier's predictions. Ask it to propose an explanation and a photograph that would test it. Take that photograph and run the classifier. Did its explanation predict the result? A friend can play detective too.

Keep some images hidden from the detective while you develop the experiment. Explain exactly what it received: images, predictions, class names, code, or weights. Those are different sources of evidence.

## Follow an interesting lead

You could let the detective choose which images to query, with a small request budget. Does it learn more than randomly chosen examples? Or ask it to suggest a repair, then check both ordinary and background-swapped photographs. A repair that damages everything else is not much help.

The [API guide]({{ '/projects/api-guide/' | relative_url }}) gives small-workload costs. Save responses and bound retries; an automated investigation can make many calls.

## Could it read the weights alone?

Recent [weight-space programming experiments](https://rikiyat.github.io/blog/weight-space-programming/) make this worth trying with a tiny network. Provide the architecture, input conventions and weights, while removing revealing filenames and class labels. Ask for a specific prediction you can verify, rather than a general story about what the network understands.

Repeat with independently trained networks and an untrained control. Permuting output labels tests whether the explanation follows the network or familiar label order. An [exploratory audit](https://arxiv.org/abs/2611.08070) found some confident semantic interpretations failed such checks; this remains an investigation, not a promised capability.

Distinguish reading weights without running the network from using tools to query it. If the AI edits weights, compare against the unchanged network on fresh examples, and record the cost and information it used. A clear account of where its explanation fails can be the most useful result.
