---
layout: page
title: Team
subtitle: Faculty, researchers, and students
permalink: /team/
---

{% assign people = site.data.team | default: [] %}
{% if people.size > 0 %}
<div class="grid cols-3">
  {% for person in people %}
  <article class="card">
    {% if person.photo %}
      <img src="{{ person.photo | relative_url }}" alt="{{ person.name }}" style="width:100%; height:auto; border-radius:8px;">
    {% endif %}
    <h3>{{ person.name }}</h3>
    <p class="muted">{{ person.role }}</p>
    {% if person.expertise %}<p>{{ person.expertise }}</p>{% endif %}
    <p>
      {% if person.email %}<a href="mailto:{{ person.email }}">Email</a>{% endif %}
      {% if person.website %} · <a href="{{ person.website }}" target="_blank" rel="noopener">Website</a>{% endif %}
      {% if person.scholar %} · <a href="{{ person.scholar }}" target="_blank" rel="noopener">Google Scholar</a>{% endif %}
      {% if person.linkedin %} · <a href="{{ person.linkedin }}" target="_blank" rel="noopener">LinkedIn</a>{% endif %}
      {% if person.twitter %} · <a href="{{ person.twitter }}" target="_blank" rel="noopener">X</a>{% endif %}
    </p>
  </article>
  {% endfor %}
  </div>
{% else %}
<p class="muted">Team profiles will appear here.</p>
{% endif %}


