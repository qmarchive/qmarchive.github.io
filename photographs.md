---
layout: default
title: "Photographs — QUỐC MẠNH"
---
<div class="article-wrap">
  <a class="back" href="{{ '/' | relative_url }}">← home</a>
  <h1>PHOTOGRAPHS</h1>
  <div class="photo-grid">
  {% assign photos = site.photos | sort: "date" | reverse %}
  {% for photo in photos %}
    <a href="{{ photo.url | relative_url }}" class="photo-card">
      {% if photo.image %}<img src="{{ photo.image | relative_url }}" alt="{{ photo.title }}">{% endif %}
      <span>{{ photo.title }}</span>
    </a>
  {% endfor %}
  </div>
</div>
