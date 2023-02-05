---
layout: page
title: Home
id: home
permalink: /
---

# 안녕하세요! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  이곳은 세영이의 디지털 가든입니다. 제가 제텔카스텐(Zettelkasten)한 메모들을 읽어볼 수 있어요.  <span style="font-weight: bold">[[Seyoung's Digital Garden]]</span> 에서 즐거운 시간 보내세요! 
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
