---
layout: student-project
permalink: /projects/offline-voice/
title: "Build an offline voice assistant"
description: "Build a local speech pipeline, measure end-to-end response delay, and improve speed while checking recognition, playback, and interruption failures."
project_fit: "You are comfortable debugging Python and want to learn how several imperfect components become a working system."
project_resources: "A microphone, headphones, and a computer that can run small speech and text models. Real-time performance depends strongly on hardware."
---

Build a spoken assistant that hears a question and speaks a response entirely on your own machine. Once it works, find out where the time goes and improve the slowest part.

The target is a reliable, measured system on the hardware you have. A reply that begins in under a second is an optional stretch goal, not a promise or an entry requirement. Even a slower system can teach you a great deal if you can explain its limits.

## First session: get one round trip working

Start with push-to-talk and a short English question. Connect three components in sequence: speech recognition, a small local text model, and text-to-speech. Use headphones so that the assistant does not transcribe its own speaker output. Print and save the intermediate transcript and text response.

Possible starting components are multilingual Whisper through [faster-whisper](https://github.com/SYSTRAN/faster-whisper), a small model through [llama.cpp](https://github.com/ggml-org/llama.cpp), and [Kokoro](https://github.com/hexgrad/kokoro) for speech output. Read their current installation requirements and licences. Start by running each component's smallest example independently.

**Check before proceeding:** Can you complete one exchange reliably? If the full pipeline does not fit in memory, use smaller models or first run the stages separately on saved audio. Make the smallest version work before learning a large voice-agent framework.

## Milestone 1: define and measure latency

Create about 20 short test utterances, including questions, pauses, corrections, and background noise. Write down the expected behaviour for each. Keep a development subset and a held-out subset; keep versions of the same utterance together.

Measure from the **actual end of the user's speech to the first audible reply**. Include the delay in deciding that speech has ended, recognition, text generation, synthesis, and playback buffering. Time to the first text token alone is not conversational latency. If you cannot directly measure audible onset, label the software timestamp as a proxy and check it against a recording.

Record per-stage timestamps, hardware, model versions, precision, context length, and response length. Report median delay, a tail measure such as the 90th percentile, and failures. With very few trials, also show individual timings. Measure cold startup separately from warm requests; cached model loading can change the experience substantially.

**Deliverable:** a latency table and a few saved examples that explain it. Choose a realistic speed target only after seeing the baseline.

## Milestone 2: improve one bottleneck

Change one component or setting at a time: a smaller recogniser, shorter replies, earlier text-to-speech chunks, or streaming generation. Compare on the same development utterances, with the same response constraints.

Measure quality as well as speed. Did the recogniser miss a name? Did early speech output say something later text would have corrected? Does cutting the response length make the assistant unhelpful? Keep a simple rubric for whether the transcript, response, and audible output are usable.

**Check before proceeding:** A faster median is not an improvement if many requests fail or longer pauses are mistaken for the end of a turn. Keep timeouts and failed requests in the report.

## Milestone 3: add natural stopping and prove it is offline

Replace push-to-talk with a voice activity detector such as [Silero VAD](https://github.com/snakers4/silero-vad). VAD marks speech and silence; it does not know whether a sentence is finished. Begin with a documented silence-duration threshold, tune it on development examples, and keep it fixed for evaluation. Test long pauses, background noise, a quiet voice, and an unfinished sentence. Measure premature replies and missed turns alongside latency. Automatic endpoint detection should earn its place through this comparison.

Download all necessary assets, then disable network access and repeat your tests. Check that no component silently falls back to a remote API. Run the fixed held-out utterances after choosing settings. Keep a small log with `utterance_id`, timings, transcript, response, quality judgement, and failure reason.

**Human judgement:** Listen to the actual conversations. Numbers cannot tell you whether an interruption is irritating, whether a response sounds complete, or whether the assistant speaks before you have finished thinking.

## A solid stopping point

A working offline demo, a baseline-versus-improved timing report, and a clear account of quality trade-offs on your machine. Include startup cost, memory use if measurable, and conditions that still break the interaction. A one-minute demo should include at least one imperfect exchange, not just a rehearsed success.

If your computer cannot run the whole pipeline interactively, a measured sequential prototype remains useful. Say explicitly which parts run offline, which run live, and which were demonstrated only with saved audio. A cloud notebook can help test a component, but it does not demonstrate an offline laptop assistant.

## Choose one extension

- Let the user interrupt: stop playback, cancel queued speech, and listen to the new turn. Test with headphones before tackling speaker echo.
- Add Tamil or another language after checking that each component supports it; measure the new bottleneck.
- Build a repeatable turn-taking test with silence, hesitations, and overlapping speech.

Keep the assistant conversational initially. Giving it control over files or accounts is a separate project and is unnecessary for studying timing.
