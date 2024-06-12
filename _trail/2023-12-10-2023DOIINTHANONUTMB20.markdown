---
layout: default
title:  "2023 DOI INTHANON By UTMB 20KM"
name: "2023INTHANON20"
description: 用脚步丈量世界
date:   2023-12-10
place: CHIANGMAI/THAILAND
bib: "2031"
time: "04:18:31"
memo: 泰国清迈UTMB50+20背靠背抢双倍石头
categories: trail
permalink: /trail/2023INTHANONUTMB20.html
max_iterations: 1
---
[back](/trail)

比赛时间：{{ page.date | date: "%Y-%m-%d" }}

比赛地点：{{ page.place }}

比赛名称：{{ page.title }}

参赛号码：{{ page.bib}}

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

[back](/trail)
