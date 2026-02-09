---
layout: page
title: Resources
subtitle: Datasets, software, and tools
permalink: /resources/
---

{% assign res = site.data.resources | default: [] %}
{% if res.size > 0 %}
<div class="grid cols-2">
  {% for r in res %}
  <article class="card">
    <h3>{{ r.name }}</h3>
    <p class="muted">{{ r.type }}</p>
    {% if r.description %}<p>{{ r.description }}</p>{% endif %}
    {% if r.links %}
      <p>
        {% for l in r.links %}<a href="{{ l.url }}" target="_blank" rel="noopener">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}{% endfor %}
      </p>
    {% endif %}
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">Resources will appear here.</p>
{% endif %}



