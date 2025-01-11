---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
  <main>
      {% assign total_posts = site.marathon | size %}
      {% assign sorted_posts = site.marathon | sort: 'date' | reverse %}
     {% for post in sorted_posts %}
         {%  if post.title contains "半马" %}
            {% assign half = half | plus:1 %}
          {%  endif %}
      {% endfor %}
 

    <h3>向百马王子进军({{ total_posts }}) [含半马{{ half }}]</h3>
    <ul>
      {% assign sorted_posts = site.marathon | sort: 'date' | reverse %}
     {% for post in sorted_posts %}
        <li>
          <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a> [{{ post.time }}]
        </li>
      {% endfor %}
    </ul>
  </main>