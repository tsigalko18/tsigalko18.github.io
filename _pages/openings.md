---
layout: page
permalink: /openings/
title: openings
description: Positions, theses, and visits at the Automated Software Testing (AST) group.
nav: true
nav_order: 4
# Add open positions here; each needs a title and a short description, and optionally a url.
positions: []
---

Thank you for your interest in joining the AST group. I receive many emails about positions, so please read this page before writing. **Emails that do not follow the instructions below will likely not get a reply.**

#### Open Positions

{% if page.positions.size > 0 %}
{% for p in page.positions %}
<div class="mt-3">
  <strong>{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}</strong>
  <br>{{ p.description }}
</div>
{% endfor %}
{% else %}
There are no open positions at the moment. New positions are announced on this page as soon as funding is available, so there is no need to email me to ask whether something is open.
{% endif %}

#### PhD Students

PhD positions are funded through specific projects and are announced above. If a position is open, apply by email with the subject line **[AST PhD] Your Name** and include:

+ your CV
+ transcripts of your BSc and MSc degrees
+ a short statement (max. one page) on which of our [research themes](/) you want to work on and why
+ links to your MSc thesis, publications, or code, if available

#### Postdocs

If you want to apply for your own fellowship to join the group (e.g., [Humboldt Research Fellowship](https://www.humboldt-foundation.de/en/apply/sponsorship-programmes/humboldt-research-fellowship) or [Marie Skłodowska-Curie Postdoctoral Fellowship](https://marie-sklodowska-curie-actions.ec.europa.eu/actions/postdoctoral-fellowships)), email me well before the deadline with the subject line **[AST Postdoc] Your Name**, your CV, and a short research proposal.

#### Theses (TUM Students)

We supervise BSc and MSc theses, guided research projects, and interdisciplinary projects on testing AI-enabled systems and AI for software testing. See the [group page](/group/) for completed theses and our [publications](/publications/) for current topics. Email me with the subject line **[AST Thesis] Your Name**, your transcript, and the topics you are interested in.

Our seminars and practical courses are listed on the [teaching page](/teaching/) and are assigned through the TUM matching system.

#### Visiting Students

We host visiting PhD students who bring their own funding (e.g., from their home university or a scholarship) and whose research fits our themes. Email me with the subject line **[AST Visit] Your Name**, your CV, the planned period, and a short description of what you want to work on.
