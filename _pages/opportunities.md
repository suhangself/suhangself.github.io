---
permalink: /opportunities/
title: "Opportunities"
author_profile: true
layout: single
---

I occasionally post **open positions** (PhD / intern / visiting), **service roles** (chair / committee), and also **forward opportunities** for friends or collaborators.

- Each item is posted with a date.
- Click the title to view details (or jump to an external page if provided).

---

{% assign items = site.opportunities | sort: "date" | reverse %}

{% for op in items %}
### {% if op.link %}<a href="{{ op.link }}" target="_blank" rel="noopener">{{ op.title }}</a>{% else %}<a href="{{ op.url | relative_url }}">{{ op.title }}</a>{% endif %}

<span style="opacity:0.85;">
<strong>Posted on:</strong> {{ op.date | date: "%Y-%m-%d" }}
{% if op.category %} &nbsp;|&nbsp; <strong>Category:</strong> {{ op.category }}{% endif %}
{% if op.source %} &nbsp;|&nbsp; <strong>Source:</strong> {{ op.source }}{% endif %}
{% if op.deadline %} &nbsp;|&nbsp; <strong>Deadline:</strong> {{ op.deadline }}{% endif %}
</span>

{% if op.excerpt %}
<br/>
{{ op.excerpt }}
{% endif %}

<hr />
{% endfor %}
