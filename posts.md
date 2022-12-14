---
layout: default
title: Posts
---

{% for post in posts %}

  <div class="post-preview">
    <div class="d-flex justify-content-between pr-xl-2">
      <h1><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h1>
      {% if post.pin == true %}
        <i class="fas fa-thumbtack fa-fw text-muted mt-1 ml-2 mt-xl-2" data-toggle="tooltip" data-placement="left"
        title="Pinned"></i>
      {% endif %}
    </div>
    <div class="post-content">
      <p>
        {% include no-linenos.html content=post.content %}
        {{ content | markdownify | strip_html | truncate: 200 }}
      </p>
    </div>

    <div class="post-meta text-muted">
      <!-- posted date -->
      <i class="far fa-clock fa-fw"></i>
      {% include timeago.html date=post.date tooltip=true %}

      <!-- page views -->
      {% if site.google_analytics.pv.enabled %}
      <i class="far fa-eye fa-fw"></i>
      <span id="pv_{{-post.title-}}" class="pageviews">
        <i class="fas fa-spinner fa-spin fa-fw"></i>
      </span>
      {% endif %}
    </div>
  </div> <!-- .post-review -->

{% endfor %}