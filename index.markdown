---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

  <main>
    <h3>用脚步丈量世界</h3>
    <ul>
      {% for post in site.posts %}
        <li>
          <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>

    <h3>TODO</h3>
    <ul>
        <li>UTMB/UTMB</li>
        <li>FUJI 168</li>
        <li>WSER/100M</li>
        <li>八百流沙</li>
        <li>拉萨马拉松</li>
        <li>环青海湖七天七马</li>
    </ul>
  </main>

  <footer>
    <p>&copy; {{ site.time | date: '%Y' }} {{ site.title }}. All rights reserved.</p>
  </footer>
