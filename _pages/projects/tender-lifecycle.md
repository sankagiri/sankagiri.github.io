---
layout: student-project
permalink: /projects/tender-lifecycle/
title: "Follow a public tender through its life"
description: "Build an evidence-backed timeline of procurement notices, revisions, cancellations, and published awards, then analyse delays and missing information."
project_fit: "You like public-interest data, document processing, and the detective work of joining imperfect records."
project_resources: "An ordinary laptop and a small permitted collection of public tender documents. Start with manual downloads."
project_budget: "₹0–3,000 for optional storage or model usage; paid tools are not needed for the seed."
---

A public tender can have an eventful life: a notice, revised deadlines, a cancellation, a retender, and perhaps an award. Can you piece that story together? What can the public record tell you about how the process works?

This is part data analysis, part document detective work. You might discover a useful pattern—or find that the records do not support the question you originally wanted to answer.

## Follow one tender

Start with the [Central Public Procurement Portal's ePublishing site](https://eprocure.gov.in/epublish/app?page=Home&service=page). Choose a tender and look for its notices, corrigenda and latest published status. Make a timeline, keeping the tender identifier and a source link for each event. Preserve original deadlines as well as revisions.

Notice the difference between when something happened, when its document was published, and when you downloaded it. If a later document has a different identifier, a similar title alone is not enough to join the records. Ask a friend whether they can reconstruct your timeline from the evidence.

## Let a question emerge

You could ask how often deadlines are extended, which kinds of revisions recur, or how long it takes for an award to appear. Choose a manageable slice, such as one organisation during a particular period, and include incomplete cases. Selecting only tenders with visible awards will give a misleading picture of waiting times.

Once you understand the documents, try automating the dull parts. Compare a simple date-and-identifier parser with AI-assisted extraction. Require a supporting page or passage and allow “not found.” Check the method on documents you did not use while improving it; a correct number attached to the wrong tender is still an error.

Use permitted downloads or exports, respect access limits, and use a smaller manual sample if a CAPTCHA blocks automation. Keep personal contact details out of anything you publish.

## Be careful about what is missing

A tender still known to be open when you stop observing has no completed award time. You know only that its observed waiting time is at least that long; statistical methods call this *censoring*. That differs from a record whose outcome is simply unknown because publication coverage is incomplete.

A missing award notice does not establish that work was never awarded. Nor does a long delay or repeated vendor name establish wrongdoing. Investigate definitions and missingness before interpreting anomalies.

A source-linked timeline explorer could be useful by itself. With better coverage and procurement expertise, you could later study waiting times or forecast delays using only information available at the prediction date. Training a neural network is not necessary for a worthwhile first investigation.

**API option:** Compare a hosted model with your local or simpler approach. See [small experiment costs and ideas]({{ '/projects/api-guide/' | relative_url }}) for Sarvam speech/text APIs and frontier models.
