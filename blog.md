---
layout: default
title: Blog
description: Cybersecurity insights, Essential 8 updates, and offensive security perspectives from Rampart Vantage.
permalink: /blog/
---

<!-- PAGE HERO -->
<section class="page-hero">
  <div class="container">
    <span class="tag">Insights</span>
    <h1>Blog</h1>
    <p class="page-subtitle">
      Practical cybersecurity writing for Australian businesses.
      No hype, no vendor fluff.
    </p>
  </div>
</section>

<!-- BLOG LIST -->
<section class="section">
  <div class="container">

    {% if site.posts.size > 0 %}

      <div class="post-list">
        {% for post in site.posts %}
          <article class="post-card">

            <div class="post-meta">
              <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
              {% if post.categories %}
                <div class="post-categories">
                  {% for category in post.categories %}
                    <span class="post-category">{{ category }}</span>
                  {% endfor %}
                </div>
              {% endif %}
            </div>

            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>

            <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>

            <a href="{{ post.url | relative_url }}" class="read-more">Read more &rarr;</a>

          </article>
        {% endfor %}
      </div>

    {% else %}

      <div class="blog-empty">
        <p>No posts yet — check back soon.</p>
      </div>

    {% endif %}

  </div>
</section>