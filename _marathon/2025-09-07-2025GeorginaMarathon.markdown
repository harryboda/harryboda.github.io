---
layout: default
title:  "2025 Georgina Marathon（300官方兔子）"
name: "2025GeorginaMarathon"
description: 用脚步丈量世界
date:   2025-09-07
place: Georgina/Canada
bib: 506
time: "02:59:30"
memo: 首次300兔子，完美完成
categories: marathon
max_iterations: 1
---
[back](/marathon)

比赛时间：{{ page.date | date: "%Y-%m-%d" }}

比赛地点：{{ page.place }}

比赛名称：{{ page.title }}

完赛成绩：{{ page.time }}

备注：{{ page.memo }}

完赛证书：
![Octocat](/images/{{ page.name }}/{{ page.name }}.png)

精彩瞬间：
<ul>
{% assign max = page.max_iterations | plus: 0 %}
{% for i in (1..max) %}
    <li><img src="/images/{{ page.name }}/{{ page.name }}-{{ i }}.jpeg"></li>
{% endfor %}
</ul>

[back](/marathon)
