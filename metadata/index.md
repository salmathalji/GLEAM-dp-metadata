---
layout: default
title: Metadata
---

<h1>GLEAM Metadata Schema</h1>

<ul>
  {% assign schema = site.data.gleam-dp-profile %}
  {% assign props = schema.allOf[1].properties %}
  {% assign required = schema.allOf[1].required %}

  {% for item in props %}
    <li>
      <strong>{{ item[0] }}</strong>
      {% if required contains item[0] %}<span style="color: red">*</span>{% endif %}<br>
      {{ item[1].description }}
    </li>
  {% endfor %}
</ul>
