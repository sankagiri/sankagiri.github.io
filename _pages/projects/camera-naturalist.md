---
layout: student-project
permalink: /projects/camera-naturalist/
title: "What does your camera model really recognise?"
description: "Collect your own leaf and flower images and investigate what a small vision model learns."
project_resources: "A phone, an ordinary laptop, and plants you can revisit. Basic Python helps; AI can help you start."
project_budget: "₹0 with existing equipment; a paid model API is optional."
---

Photograph a few kinds of leaves or flowers near home. Teach a model to tell them apart. Now visit another garden: does it still work? Perhaps it recognised the plant—or perhaps it recognised your balcony wall.

This is a good first project for a school or first-year college student. You can begin without knowing species names: “plant A” and “plant B” are useful labels until someone knowledgeable checks the identification.

## Try this first

Choose a few visibly different plants and photograph several individuals of each kind. Include different views and lighting, and record which plant each photo came from. Leave plants undisturbed; ask permission where needed.

Use a pretrained small vision model to turn each image into a list of numbers, called an embedding. Find the most similar photographs, then try a simple classifier. [DINOv2's small ViT](https://github.com/facebookresearch/dinov2) is one option. Keep its weights fixed and save the embeddings: you can experiment with classifiers without running the image model again. Try a handful of images first to check your laptop's speed. Training a ViT from scratch is unnecessary.

Keep whole individual plants aside for testing. Twenty photographs of one leaf are still observations of one leaf.

## Follow what puzzles you

Does changing the background change the answer? Compare close crops with wider photographs, or photograph naturally fallen leaves against different surfaces. Check the altered photographs yourself: cropping might remove useful leaf shape as well as background.

What happens to wet leaves, unopened flowers, shadows, or a plant the model has never seen? Can it say “uncertain” instead of confidently forcing everything into a familiar category? A tiny CNN trained on your images makes an interesting comparison with the pretrained ViT.

Plants are only one possibility. Photograph arrangements of seeds or buttons and investigate counting: does a new arrangement confuse the model even when the number stays the same?

## Make one discovery you can explain

Keep mistaken predictions beside correct ones. Change one suspected clue and take fresh photographs to test your explanation. A high score on near-duplicate images tells you little about another garden.

You could compare with a vision API, or predict visible attributes such as colour and leaf shape. Passing an arbitrary embedding to a text model does not automatically teach it to see. Retrieving labelled examples is an easier starting point; learning a connection to a language model is a deeper extension.

If investigating the classifier becomes more interesting than identifying plants, continue with [can one AI investigate another?]({{ '/projects/model-detective/' | relative_url }}).
