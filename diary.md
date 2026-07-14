---
layout: page
title: "日常"
permalink: /diary.html
---
### 日記列表
<ul>
  {% assign sorted_diaries = site.diaries | sort: 'date' | reverse %}
  {% for diary in sorted_diaries %}
    <li style="margin-bottom: 12px; list-style-type: none; border-bottom: 1px dashed #e1e4e8; padding-bottom: 8px;">
      <span style="color: #666; font-size: 0.9em; margin-right: 15px;">
        {{ diary.date | date: "%Y-%m-%d" }}
      </span>
      <a href="{{ diary.url }}" style="color: #0366d6; text-decoration: none; font-weight: bold;">
        {{ diary.title }}
      </a>
    </li>
  {% endfor %}
</ul>
