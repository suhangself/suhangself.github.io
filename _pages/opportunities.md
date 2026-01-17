---
permalink: /opportunities/
title: "Opportunities"
author_profile: true
layout: single
---

We regularly have openings for **PhD**, **interns**, and **visiting students**.

{% assign items = site.opportunities | sort: "date" | reverse %}

{% for op in items %}
### {{ op.title }}

**Posted on:** {{ op.date | date: "%Y-%m-%d" }}
{% if op.type %} | **Type:** {{ op.type }}{% endif %}
{% if op.deadline %} | **Deadline:** {{ op.deadline }}{% endif %}
{% if op.location %} | **Location:** {{ op.location }}{% endif %}

{% if op.external_url %}
- <a href="{{ op.external_url }}" target="_blank" rel="noopener">Apply / External link</a>
{% endif %}
- <a href="{{ op.url | relative_url }}">Details</a>

<hr />
{% endfor %}
