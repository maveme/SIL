---
layout: page
title: Publications
subtitle: Selected papers and presentations
permalink: /publications/
---

{% assign pubs = site.data.publications | default: [] %}
{% if pubs.size > 0 %}
<div class="grid cols-1">
  {% for p in pubs %}
  <article class="card">
    <h3>{{ p.title }}</h3>
    <p class="muted">{{ p.authors }} — {{ p.venue }} ({{ p.year }})</p>
    {% if p.abstract %}<p>{{ p.abstract }}</p>{% endif %}
    <p>
      {% if p.doi %}<a href="https://doi.org/{{ p.doi }}" target="_blank" rel="noopener">DOI</a>{% endif %}
      {% if p.url %} {% if p.doi %}·{% endif %} <a href="{{ p.url }}" target="_blank" rel="noopener">Link</a>{% endif %}
      {% if p.pdf %} · <a href="{{ p.pdf | relative_url }}" target="_blank" rel="noopener">PDF</a>{% endif %}
      {% if p.code %} · <a href="{{ p.code }}" target="_blank" rel="noopener">Code</a>{% endif %}
    </p>
  </article>
  {% endfor %}
</div>
{% else %}
<p class="muted">Publications will appear here.</p>
{% endif %}
