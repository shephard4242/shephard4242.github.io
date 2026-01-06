---
layout: default
title: Home
---

<h1>Projects</h1>

<div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:16px;">
  {% for p in site.projects %}
    <a href="{{ p.url | relative_url }}" style="text-decoration:none;color:inherit;border:1px solid #ddd;border-radius:12px;overflow:hidden;display:block;">
      {% if p.cover %}
        <img src="{{ p.cover | relative_url }}" alt="{{ p.title }}" style="width:100%;height:160px;object-fit:cover;display:block;">
      {% endif %}
      <div style="padding:12px;">
        <div style="font-weight:600;">{{ p.title }}</div>
        {% if p.description %}
          <div style="opacity:.8;font-size:.95em;margin-top:6px;">{{ p.description }}</div>
        {% endif %}
      </div>
    </a>
  {% endfor %}
</div>
