---
layout: default
title: ""
---

<div class="intro">
  <p>{{ site.description }}</p>
</div>

<section class="posts-list">
  <h2 class="section-title">Все статьи</h2>

  {% for post in site.posts %}
    <article class="post-preview">
      <div class="post-preview-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%d %b %Y' }}</time>
      </div>
      <h3 class="post-preview-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      {% if post.tags.size > 0 %}
        <div class="post-preview-tags">
          {% for tag in post.tags %}
            <span class="tag">{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
      {% if post.description %}
        <p class="post-preview-description">{{ post.description }}</p>
      {% endif %}
    </article>
  {% endfor %}
</section>
