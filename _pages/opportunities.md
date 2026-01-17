---
permalink: /opportunities/
title: "Opportunities"
author_profile: true
layout: single
---

I occasionally post open positions (PhD / intern / visiting), service roles (chair / committee), and also forward opportunities for friends or collaborators.

- Each item is posted with a date.
- Click the title to view details (or jump to an external page if provided).

---

{% assign items = site.opportunities | sort: "date" | reverse %}

{% for op in items %}
### {% if op.link %}
<a href="{{ op.link }}" target="_blank" rel="noopener">{{ op.title }}</a>
{% else %}
<a href="{{ op.url | relative_url }}">{{ op.title }}</a>
{% endif %}

**Posted on:** {{ op.date | date: "%Y-%m-%d" }}
{% if op.deadline %} &nbsp;|&nbsp; **Deadline:** {{ op.deadline }}{% endif %}

<hr />
{% endfor %}
