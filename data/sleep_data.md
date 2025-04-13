---
layout: default
title: Sleep_data Schema
---

<h2>Sleep_data Schema</h2>

{% assign schema = site.data["sleep_data.schema.json"] %}

<ul>
  {% for field in schema.fields %}
    <li>
      <strong>{{ field.name }}</strong> ({{ field.type }})<br>
      {% if field.description %}<em>{{ field.description }}</em>{% endif %}
    </li>
  {% endfor %}
</ul>
