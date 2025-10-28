---
layout: page
title: Research Areas
subtitle: Our core topics and methods
permalink: /research-areas/
---

{% assign areas = site.data.areas | default: [] %}
{% if areas.size > 0 %}
<div class="grid cols-2">
  {% for area in areas %}
  <article class="card">
    <h3>{{ area.name }}</h3>
    <p class="muted">{{ area.tagline }}</p>
    <p>{{ area.description }}</p>
    {% if area.keywords %}
      <p>
        {% for k in area.keywords %}<span class="chip">{{ k }}</span> {% endfor %}
      </p>
    {% endif %}
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">Research areas will appear here.</p>
{% endif %}