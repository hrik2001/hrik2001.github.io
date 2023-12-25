---
layout: index
title: Blog
---

# Blog Archive

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
      <div class="post-categories">
        Categories:
        {% for category in post.categories %}
          <span>{{ category }}</span>
          {% unless forloop.last %},{% endunless %}
        {% endfor %}
      </div>
    </li>
  {% endfor %}
</ul>
