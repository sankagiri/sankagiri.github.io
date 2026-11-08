---
permalink: /projects/
title: "Build, measure, understand"
description: "Twenty independent science and data projects: affordable instruments, real-world experiments, checked simulators, public data, and AI."
author_profile: true
---

You do not need an internship to start doing interesting work. Turn a flowerpot into a water-balance experiment, draw an object with echoes, investigate your street's traffic, or teach a model to control a simulated room. Here are **20 projects in five themes**, with small beginnings and room to go much further.

**Use AI tools generously.** Let them help with code, electronics, unfamiliar mathematics, and debugging. You supply the curiosity, experimental choices, and checks.

<nav class="project-links" aria-label="On this page">
  <a href="#choose-a-project">Choose a project</a>
  <a href="{{ '/projects/working-guide/' | relative_url }}">Working guide</a>
  <a href="{{ '/projects/instrument-guide/' | relative_url }}">Instruments and budgets</a>
  <a href="{{ '/projects/api-guide/' | relative_url }}">Model APIs and costs</a>
  <a href="#getting-in-touch">When to get in touch</a>
</nav>

<aside class="project-note" aria-label="About these projects" markdown="1">
**These are independent projects, not supervised internships.** You do not need my permission to begin. I cannot provide individual supervision or debugging help, but I would be glad to hear about a carefully investigated result once you have made substantial progress.
</aside>

## Choose a project
{: #choose-a-project }

These are starting points, not assignments. Try something small, follow what puzzles you, and change direction when you find a better question. You do not need to complete every suggestion.

**Unsure where to begin?** Try [flow visualisation]({{ '/projects/flow-visualisation/' | relative_url }}) with your phone, [pot drying]({{ '/projects/soil-water/' | relative_url }}) with a balance, or a [queue simulator]({{ '/projects/queue-lab/' | relative_url }}) on a laptop. Buying equipment is optional. The budgets below are estimated starter-kit totals, excluding an existing phone/laptop; see the [instrument guide]({{ '/projects/instrument-guide/' | relative_url }}) before buying.

<nav class="project-theme-nav" aria-label="Project themes">
{% for theme in site.data.project_themes %}
  <a href="#{{ theme.id }}">{{ theme.title }}</a>
{% endfor %}
</nav>

{% for theme in site.data.project_themes %}
<section class="project-theme" aria-labelledby="{{ theme.id }}">
<h2 id="{{ theme.id }}">{{ theme.title }}</h2>
<p>{{ theme.description }}</p>
<ul class="project-list">
{% assign theme_projects = site.data.student_projects | where: 'theme', theme.id %}
{% for project in theme_projects %}
  <li>
    <h3><a href="{{ project.slug | prepend: '/projects/' | append: '/' | relative_url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
    <p class="project-meta"><strong>Start with:</strong> {{ project.resources }}</p>
  </li>
{% endfor %}
</ul>
</section>
{% endfor %}

Pick one, not a whole theme. You can adapt a language project to a language you know, or a physical experiment to the space and equipment you have. Many extensions need a partner, reference measurements, or permission to work somewhere; spending more money is not automatically the next step.

## When to get in touch
{: #getting-in-touch }

I would be glad to hear about substantial independent work. A polished demo alone is not enough; an unexpected or negative result can be, if you have investigated it carefully. **The project need not follow the original idea or be “finished.”**

Before writing, be ready to show:

- **What you found:** a clear question and evidence, with a sensible comparison where appropriate.
- **Why you trust it:** checks you made, alternative explanations you explored, and what remains uncertain.
- **Your own thinking:** decisions you made, what you learned, and how you used AI.

Email [me](mailto:{{ site.author.email }}) with the subject **“Independent project: [project name]”**. Keep the note short: state your main finding and its biggest limitation, link to code or a documented setup and a short report, and ask **one specific question**. Share only data you have permission to share; explain how someone else could check your result.

I appreciate thoughtful reports, but cannot promise a response or ongoing guidance. Please continue without waiting for me. Choose a project because you want to understand it, regardless of whether I reply.

These are not applications or supervised internships. Doing a project does not confer an IIT Madras affiliation, certificate, recommendation, or internship. For formal opportunities, the [usual application channels]({{ '/' | relative_url }}#opportunities) still apply.
