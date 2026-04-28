---
permalink: /zh/blog/
title: "博客"
excerpt: "全部博客文章"
author_profile: true
lang: zh
lang_alt: /blog/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<span class='anchor' id='blog-list'></span>

# <i class="fas fa-blog"></i> 全部文章

<div class="blog-grid">
{% assign zh_posts = site.posts | where: 'lang', 'zh' %}
{% assign sorted_posts = zh_posts | sort: 'date' | reverse %}
{% for post in sorted_posts %}
  <a href="{{ post.url | relative_url }}" class="blog-card-link">
    <div class="blog-card">
      <div class="blog-card-image">
        <div class="blog-badge">{{ post.date | date: "%Y 年 %-m 月" }}</div>
        {% if post.cover_image %}
        <img src="{{ post.cover_image | relative_url }}" alt="{{ post.title }}">
        {% else %}
        <img src="{{ '/images/default-blog-cover.jpg' | relative_url }}" alt="{{ post.title }}">
        {% endif %}
      </div>
      <div class="blog-card-content">
        <div class="blog-title">{{ post.title }}</div>
        <div class="blog-description">{{ post.description | default: post.excerpt | strip_html | truncate: 150 }}</div>
      </div>
    </div>
  </a>
{% endfor %}
</div>

{% if sorted_posts.size == 0 %}
<div class="quote-accent">
  <p>暂无博客文章，欢迎稍后回来看看！</p>
</div>
{% endif %}
