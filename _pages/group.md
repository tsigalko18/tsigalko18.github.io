---
layout: page
permalink: /group/
title: group
description: Automated Software Testing (AST) group at fortiss and TUM.
nav: true
nav_order: 3
---

Our research sits at the intersection of software engineering and AI. We build testing techniques that make AI-enabled systems, from deep learning components to autonomous vehicles and LLM-based applications, robust, reliable, and safe. Our tools and replication packages are on [GitHub](https://github.com/ast-fortiss-tum).

#### PhD Students

{% for member in site.data.group.phd %}
<div class="mt-4">
  <strong>{% if member.url %}<a href="{{ member.url }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</strong>
  · {{ member.role }} ({{ member.since }}–)
  <br><span class="text-muted">{{ member.topic }}</span>
</div>
{% endfor %}

<br>

#### Visiting Students

{% for member in site.data.group.visitors %}
<div class="mt-2">
  {% if member.url %}<a href="{{ member.url }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}{% if member.from %}
  · {{ member.from }}{% endif %}
</div>
{% endfor %}

<br>

#### Completed Theses & Student Projects

{% assign msc = 0 %}{% assign bsc = 0 %}{% assign other = 0 %}
{% for year in site.data.theses %}{% for t in year[1] %}
{% if t.type == "MSc thesis" %}{% assign msc = msc | plus: 1 %}{% elsif t.type == "BSc thesis" %}{% assign bsc = bsc | plus: 1 %}{% else %}{% assign other = other | plus: 1 %}{% endif %}
{% endfor %}{% endfor %}
Since 2023 we have supervised {{ msc }} MSc theses, {{ bsc }} BSc theses, and {{ other }} guided research projects, seminars, and internships. Many of them led to publications and open-source tools.

{% for year in site.data.theses %}
<details class="mt-3">
<summary><strong>{{ year[0] }}</strong> ({{ year[1].size }})</summary>
<ul class="mt-2">
{% for t in year[1] %}
  <li class="mb-1">
    <strong>{{ t.name }}</strong>. <i>{{ t.title }}</i>.
    <span class="text-muted">{{ t.type }}{% if t.with %}, with {{ t.with }}{% endif %}.</span>
    {% if t.repo %}<a href="{{ t.repo }}">Code</a>{% endif %}
    {% for key in t.papers %}{% assign parts = key | split: "-" %}
    {% if forloop.first and t.repo %}·{% endif %} 🏅 <a href="{{ '/publications/' | relative_url }}#{{ key }}">{{ parts[2] }} {{ parts[0] }} paper</a>
    {% endfor %}
  </li>
{% endfor %}
</ul>
</details>
{% endfor %}
