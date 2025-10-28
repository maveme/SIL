---
layout: page
title: Publications
permalink: /publications/
---

{% assign pubs = site.data.publications | default: [] %}
{% if pubs.size > 0 %}
<div class="content">
  {% for p in pubs %}
  <article class="card">
    <h3>
      {% if p.url %}<a href="{{ p.url }}" target="_blank" rel="noopener">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}
    </h3>
    <p class="muted">
      {% if p.authors %}{{ p.authors }} · {% endif %}
      {% if p.venue %}{{ p.venue }}{% endif %}
      {% if p.year %} · {{ p.year }}{% endif %}
      {% if p.doi %} · <a href="https://doi.org/{{ p.doi }}" target="_blank" rel="noopener">doi:{{ p.doi }}</a>{% endif %}
    </p>
    {% if p.abstract %}<p>{{ p.abstract }}</p>{% endif %}
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">Publication entries will appear here.</p>
{% endif %}


