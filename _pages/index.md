---
layout: page
title: Home
id: home
permalink: /
---

# 안녕하세요! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  세영이의 2번째 뇌를 보시려면 클릭! <span style="font-weight: bold">[[Seyoung's Second Brain]]</span> 
</p>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes | limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
