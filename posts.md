---
layout: default
title: Blog Posts
---

# Blog Posts

{% for post in site.posts %}

  <div>
    <div class="post-header">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <span>{{ post.date | date: "%B %-d, %Y" }}</span>
    </div>
    <div class="post-excerpt">
      <p>
        {{ post.content | markdownify | strip_html | truncate: 200 }}
      </p>
    </div>
  </div>
  <hr />

{% endfor %}