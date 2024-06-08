---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
  <main>
    <h3>向百马王子进军</h3>
    <ul>
      {% assign sorted_posts = site.marathon | sort: 'date' | reverse %}
      {% for post in sorted_posts %}
        <li>
          <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>

  </main>