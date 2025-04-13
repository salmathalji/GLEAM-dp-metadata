---
layout: default
title: Dataset Schema
---

<h2>Dataset Schema</h2>

{% assign schema = site.data["dataset.schema"] %}

<ul>
  {% for field in schema.fields %}
    <li>
      <strong>{{ field.name }}</strong> ({{ field.type }})<br>
      {% if field.description %}<em>{{ field.description }}</em>{% endif %}
    </li>
  {% endfor %}
</ul>
