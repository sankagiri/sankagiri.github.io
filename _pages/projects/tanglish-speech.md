---
layout: student-project
permalink: /projects/tanglish-speech/
title: "Can speech recognisers follow Tanglish?"
description: "Create a small Tamil–English speech evaluation with careful transcripts, explicit scoring rules, and an analysis of code-switching errors."
project_fit: "You speak Tamil, can work with another fluent listener, and enjoy careful data work."
project_resources: "A phone microphone, Python, audio tools, consenting adult speakers, and time to transcribe. Small-model inference can start on a CPU."
---

Record a conversation that moves naturally between Tamil and English. What does a speech recogniser get wrong? Names, English words with Tamil endings, or the moments when the speaker switches language?

The interesting work is listening carefully and finding a pattern. You do not need hours of audio or a newly trained model to begin.

## Try this first

Record yourself explaining a hobby or a course concept for about a minute. Write down what you said **before** looking at a model's output. Run a small multilingual Whisper model, for example through [faster-whisper](https://github.com/SYSTRAN/faster-whisper), and listen to each mismatch.

Check the audio format and sample rate, and make sure the model is transcribing rather than translating. Save the original recording, your transcript, and the model's output.

## Follow a question

Collect a few more short recordings from consenting adult friends. Decide how to write Tamil, English, loan words, numbers, repetitions, and unfinished words. Have another fluent listener transcribe a sample independently. Disagreements about spelling may reveal a measurement problem before you find a model problem.

Compare two recognisers, or two settings of one recogniser. Group errors into a few useful categories. Perhaps language switches matter less than background noise or unfamiliar names; follow what the recordings suggest.

Word error rate counts inserted, deleted, and substituted words relative to the reference transcript. Check the calculation on tiny examples; it can exceed 100%. Keep examples beside the score so the reader can understand what it means.

## Keep yourself honest

- Preserve raw transcripts and document any spelling or punctuation normalisation. Do not erase difficult cases to improve the score.
- Ask separately about recording, external processing, and public release. Voices remain identifiable even when names are removed.
- If you use recordings to choose settings or train a model, test on new recordings, ideally from new speakers. Many clips from two friends are still only two speakers.
- A reference transcript can be wrong. Listen again before concluding that the recogniser failed.

## If it gets interesting

Investigate errors near language switches, false words during silence, or performance across recording conditions. Fine-tuning is an option once you have separate training and evaluation data; it need not be the next step.

The [Hugging Face Audio course](https://huggingface.co/learn/audio-course/en/chapter0/introduction) helps with practical tools, while [IndicVoices](https://arxiv.org/abs/2403.01926) provides an example of planned speech collection. A small, well-checked dataset and one clear observation can be a satisfying project. Budget mainly for listening, not compute.

**API option:** Compare a hosted model with your local or simpler approach. See [small experiment costs and ideas]({{ '/projects/api-guide/' | relative_url }}) for Sarvam speech/text APIs and frontier models.
