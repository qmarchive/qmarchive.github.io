---
layout: default
title: "Notes — QUỐC MẠNH"
---
<div class="article-wrap narrow">
  <a class="back" href="{{ '/' | relative_url }}">← home</a>
  <h1>NOTES</h1>
  {% assign notes = site.notes | sort: "date" | reverse %}
  {% for note in notes %}
  <div class="entry" style="border-top:1px dashed var(--line);padding:10px 0">
    <span>{{ note.date | date: "%d.%m.%Y" }}</span>
    <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
  </div>
  {% endfor %}
</div>
