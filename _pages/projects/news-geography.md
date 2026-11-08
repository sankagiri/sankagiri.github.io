---
layout: student-project
permalink: /projects/news-geography/
title: "Which places make the news?"
description: "Create a small permitted news index and investigate geographic coverage while auditing duplicates, locations, and sampling gaps."
project_fit: "You like language, geography, journalism, and asking what a dataset leaves out."
project_resources: "A laptop, a permitted feed or API, and time to manually label a small reference sample."
project_budget: "₹0–3k with existing computing; begin within free access and avoid paid full-archive commitments."
---

When heavy rain hits a city, which neighbourhoods make the news? Are several articles reporting different incidents, or repeating the same story? Build a small news index and investigate a slice of coverage you care about.

The distinction matters: a map of reporting is not automatically a map of flooding, crime, or public concern. Discovering how the map changes as you understand the stories could be the most interesting part.

## Start by reading a few stories

Choose a topic, place and short period. Use a publisher's permitted feed or API, or a documented index. Keep links, publishers and publication dates, and write down where each event seems to have happened. Allow “unclear” rather than forcing every story onto a map.

A Delhi dateline may introduce a story about somewhere else. Several outlets may repeat one report. Ask another reader to check your decisions about location and whether stories describe the same event.

Possible starting routes include [The Indian Express feed directory](https://indianexpress.com/rss/), the [Guardian API documentation](https://open-platform.theguardian.com/documentation/) and [access terms](https://open-platform.theguardian.com/access/), or [GDELT's data documentation](https://gdeltproject.org/data.html). Check their current conditions. A manually assembled index is enough to begin if automated access is difficult.

## Follow the gaps and repetitions

Compare simple place-name matching with a language model or another text-analysis tool. Check its suggestions against your own reading, including ambiguous names and stories mentioning several places. Test it on fresh stories; keep retellings of the same event together so they do not appear on both sides of the comparison.

Make one map counting articles and another counting distinct reported events. How much changes? Does the pattern survive removing uncertain locations? If comparing publishers, check what their feeds include: a local-news feed and a national front page cover different things.

Keep a collection log. A failed download or a feed that retains only recent items can produce a gap that looks like a quiet news day. Respect rate limits and access restrictions; do not bypass paywalls or CAPTCHAs. Share source links and permitted derived results rather than assuming you may republish article text or images.

## A question to grow into

You could compare language editions, follow one event across outlets, or build a model that flags locations needing human review. Your direction may change as you read.

To estimate which real incidents went unreported, you would need a separate, reasonably complete event record, such as a suitable municipal log—and an understanding of its gaps too. Without that, describe the result as coverage within your chosen sources and period. More scraping cannot supply the missing denominator.
