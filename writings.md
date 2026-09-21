---
layout: default
title: "Writings — QUỐC MẠNH"
---
<div class="article-wrap">
  <a class="back" href="{{ '/' | relative_url }}">← home</a>
  <h1>WRITINGS</h1>
  {% for post in site.posts %}
  <div class="entry" style="border-top:1px dashed var(--line);padding:10px 0">
    <span>{{ post.date | date: "%d.%m.%Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </div>
  {% endfor %}
</div>
