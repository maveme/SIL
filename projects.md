---
layout: page
title: Projects
subtitle: Current and past research initiatives
permalink: /projects/
---

{% assign projs = site.data.projects | default: [] %}
{% if projs.size > 0 %}
<div class="grid cols-2">
  {% for pr in projs %}
  <article class="card">
    <h3>{{ pr.name }}</h3>
    <p class="muted">{{ pr.period }}{% if pr.role %} · {{ pr.role }}{% endif %} {% if pr.team %} · {{ pr.team }}{% endif %}</p>
    {% if pr.objectives %}<p>{{ pr.objectives }}</p>{% endif %}
    {% if pr.outcomes %}<p><strong>Outcomes:</strong> {{ pr.outcomes }}</p>{% endif %}
    {% if pr.links %}
      <p>
        {% for l in pr.links %}<a href="{{ l.url }}" target="_blank" rel="noopener">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}{% endfor %}
      </p>
    {% endif %}
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">Project information will appear here.</p>
{% endif %}



