---
layout: page
title: News & Events
subtitle: Updates, talks, workshops, and conferences
permalink: /news/
---

{% assign items = site.data.news | default: [] %}
{% if items.size > 0 %}
<div class="grid cols-1">
  {% for n in items %}
  <article class="card">
    <h3>{{ n.title }}</h3>
    <p class="muted">{{ n.date }}{% if n.location %} — {{ n.location }}{% endif %}</p>
    {% if n.summary %}<p>{{ n.summary }}</p>{% endif %}
    {% if n.links %}
      <p>
        {% for l in n.links %}<a href="{{ l.url }}" target="_blank" rel="noopener">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}{% endfor %}
      </p>
    {% endif %}
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">News and events will appear here.</p>
{% endif %}


