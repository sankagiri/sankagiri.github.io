---
layout: student-project
permalink: /projects/survey-gaps/
title: "Which district comparisons survive a closer look?"
description: "Build an audited comparison of NFHS district indicators, checking definitions, geographic boundaries, sample-size flags, and limits on interpretation."
project_fit: "You enjoy statistics, maps, and asking whether an attractive chart actually supports its conclusion."
project_resources: "An ordinary laptop, public NFHS fact sheets, and patience with definitions and messy tables. The starter needs no household microdata approval."
project_budget: "₹0 beyond an existing laptop and internet access."
---

A map suggests that a district improved dramatically between two surveys. Did life change, or did the district boundary, population being measured, or definition of the indicator change? Investigate a comparison that interests you, and let readers inspect the evidence behind it.

You might start with sanitation or electricity access in your own state. NFHS-4 and NFHS-5 make a useful specified comparison; the aim is to understand the data, not necessarily to use the newest release.

## Start with a few numbers you can check

Find public fact sheets through the [IIPS publications page](https://www.nfhsiips.in/nfhsuser/publication.php), or try the [official NFHS-5 district catalogue](https://www.data.gov.in/catalog/national-family-health-survey-5-nfhs-5-india-districts-factsheet-data-provisional). Pick one indicator and trace a few values back to their source pages. Record what the indicator actually means, who it describes, and any symbols beside the number.

Parentheses, asterisks and blanks matter: some estimates come from small samples, and others are suppressed. Missing does not mean zero. AI can help extract tables, but compare its output with values you have checked yourself before trusting a whole spreadsheet.

## Follow the surprising comparisons

Choose districts whose boundaries can be matched between rounds. Similar names do not guarantee the same area. When a district has split, averaging its successors' percentages does not reconstruct the old figure unless you have the appropriate population counts.

Show both rounds' values alongside their change, with links to the evidence. Does the picture change when you leave out uncertain matches or small-sample estimates? What happens if you examine a related indicator? You might find that cleaning one comparison is more interesting than making a map of the whole country.

Remember that these are surveys of different samples of people, not repeated measurements of the same households. The fieldwork dates matter, and a district-level association does not establish what caused a change. Fact sheets alone may not provide enough information to tell whether a small difference exceeds sampling uncertainty.

## A possible deeper direction

With [authorised household microdata](https://www.nfhsiips.in/nfhsuser/datarequest.php), you could reproduce a published table and ask more detailed questions. The [Guide to DHS Statistics](https://www.dhsprogram.com/pubs/pdf/DHSG1/Guide_to_DHS_Statistics_DHS-7_v2.pdf) explains why survey weights and the grouping of sampled households matter for estimates and uncertainty. That extension benefits from someone experienced in survey statistics.

The public-aggregate version needs no microdata approval. A clear, source-linked explanation of one result—and why a tempting alternative conclusion is unsupported—can be the whole project. A neural network is optional; careful statistical reasoning may be the more useful tool here.
