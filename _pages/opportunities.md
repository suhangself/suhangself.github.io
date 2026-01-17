{% assign items = site.opportunities | sort: "date" | reverse %}

{% for op in items %}
### {% if op.link %}<a href="{{ op.link }}" target="_blank" rel="noopener">{{ op.title }}</a>{% else %}<a href="{{ op.url | relative_url }}">{{ op.title }}</a>{% endif %}

**Posted on:** {{ op.date | date: "%Y-%m-%d" }}
{% if op.category %} | **Category:** {{ op.category }}{% endif %}
{% if op.source %} | **Source:** {{ op.source }}{% endif %}

{% if op.excerpt %}
{{ op.excerpt }}
{% endif %}

<hr />
{% endfor %}
