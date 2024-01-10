---
layout: default
title: Posts
---

{% for post in site.posts %}

  <div>
    <div class="post-header">
      <h1><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h1>
      <span>{{ post.date | date: "%B %-d, %Y" }}</span>
      {% if post.pin == true %}
      (Pinned)
      {% endif %}
    </div>
    <div class="post-excerpt">
      <p>
        {{ post.content | markdownify | strip_html | truncate: 200 }}
      </p>
    </div>
  </div>

{% endfor %}