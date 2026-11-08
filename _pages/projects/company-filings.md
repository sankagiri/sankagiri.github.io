---
layout: student-project
permalink: /projects/company-filings/
title: "Do companies mean the same thing by water use?"
description: "Build an evidence-backed dataset from company reports and test the comparability of environmental measures across firms and years."
project_fit: "You enjoy investigating public records and are willing to read footnotes as carefully as charts."
project_resources: "A laptop, official annual or sustainability reports, and a small hand-checked reference table."
project_budget: "₹0–3k for the core analysis with existing computing; paid data or AI services are optional."
---

Two companies say they use less water per rupee of revenue. Did they withdraw less water, earn more revenue, or change which factories their figures cover? Build your own small dataset from their reports and find out which comparisons survive a closer look.

Water is one possibility. Energy use, installed capacity, or another operating measure could be just as interesting. Let your curiosity about an industry choose the question.

## Trace a number back to its meaning

Pick a sector and read reports from a couple of companies over more than one year. Use official investor-relations archives, such as [NTPC's report page](https://ntpc.co.in/investors/annual-reports/2025-26), or sources linked from [SEBI's filings directory](https://www.sebi.gov.in/curation/corporate_filings.html).

Choose one quantity and find the table and footnote behind it. Keep the value, unit, financial year and source page together. Does it describe the company alone, its entire group, or selected sites? Ask someone else to locate the number and check your interpretation.

This small exercise may already reveal a better question than the one you started with.

## Explore the comparisons

Try plotting both total water withdrawal and withdrawal per unit of revenue. Do they tell the same story? Check whether a change comes from the numerator, the denominator, a revised figure, or a different set of operations being included.

Keep water withdrawn, consumed, discharged and recycled distinct when the reports do. Treat zero, “not reported” and “not applicable” differently. Convert units with examples you can calculate by hand. Some comparisons will remain impossible; explaining why is useful work.

AI can help extract candidate values and read unfamiliar terminology. Require a source page for every extracted value, and compare with a simple text-search or table-extraction method. Test on whole reports or companies you kept aside while developing the method. Check the year, unit and company boundary as carefully as the number itself.

## Where could this lead?

You might build a small explorer that lets readers inspect every plotted value, or study how a sector ranking changes when inconsistent definitions are removed. A learned extraction model could become useful after enough carefully labelled examples accumulate; it need not be the starting point.

A discrepancy is a prompt to investigate, not evidence of fraud or greenwashing. Likewise, these reports do not automatically make a stock-price prediction project: publication timing and selection effects can create impressive-looking but misleading results.

Keep source links and unresolved cases visible, and check reuse terms before sharing report material. More ambitious comparisons benefit from accounting or industry knowledge. A modest dataset with understandable numbers can be more valuable than a much larger one nobody can audit.

**API option:** Compare a hosted model with your local or simpler approach. See [small experiment costs and ideas]({{ '/projects/api-guide/' | relative_url }}) for Sarvam speech/text APIs and frontier models.
