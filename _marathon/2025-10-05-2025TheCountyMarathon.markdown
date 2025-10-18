---
layout: default
title:  "2025 The County Marathon乡村马拉松（345官方兔子）"
name: "2025TheCountyMarathon"
description: 用脚步丈量世界
date:   2025-10-05
place: Prince Edward/Canada
bib: 193
time: "03:44:30"
memo: 乡村马拉松，啤酒不错，全场最快的兔子居然最后差点抽筋
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
