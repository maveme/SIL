---
layout: page
title: Collaborations
subtitle: Industry and academic partners
permalink: /collaborations/
---

{% assign partners = site.data.collaborations | default: [] %}
{% if partners.size > 0 %}
<div class="grid cols-3">
  {% for c in partners %}
  <article class="card" style="display:flex;flex-direction:column;gap:0.5rem;align-items:flex-start;">
    {% if c.logo %}<img src="{{ c.logo | relative_url }}" alt="{{ c.name }} logo" style="height:48px; width:auto;">{% endif %}
    <h3>{{ c.name }}</h3>
    {% if c.description %}<p>{{ c.description }}</p>{% endif %}
    {% if c.website %}<p><a href="{{ c.website }}" target="_blank" rel="noopener">Website</a></p>{% endif %}
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">Collaboration partners will appear here.</p>
{% endif %}


