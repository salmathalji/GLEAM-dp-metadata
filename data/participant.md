---
layout: default
title: Participant Schema
---

<h2>Participant Schema</h2>

{% assign schema = site.data["participant.schema.json"] %}

<ul>
  {% for field in schema.fields %}
    <li>
      <strong>{{ field.name }}</strong> ({{ field.type }})<br>
      {% if field.description %}<em>{{ field.description }}</em>{% endif %}
    </li>
  {% endfor %}
</ul>
