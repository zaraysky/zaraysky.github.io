---
layout: default
---

<section class="hero">
  <h1 class="hero-title">Узнал — и поделился</h1>
  <p class="hero-sub">{{ site.description }}</p>
</section>

<h2 class="section-title">Все статьи</h2>
<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <div class="post-meta">
        <time class="post-date" datetime="{{ post.date | date_to_xmlschema }}">{% include ru_date.html date=post.date %}</time>
      </div>
      <h3 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      {% if post.tags and post.tags.size > 0 %}
        <div class="tags">
          {% for tag in post.tags %}
            <span class="tag">{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
      {% if post.description %}
        <p class="post-desc">{{ post.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
