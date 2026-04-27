---
layout: page
title: Posts
icon: fas fa-pen-nib
order: 3
permalink: /posts/
---

<div id="post-list">

{% for post in site.posts %}
  <article class="card-wrapper card">
    <a href="{{ post.url | relative_url }}" class="post-preview row g-0 flex-md-row-reverse">
      <div class="col-md-12">
        <div class="card-body d-flex flex-column">
          <h1 class="card-title my-2 mt-md-0">
            {{ post.title }}
          </h1>

          <div class="card-text post-content mt-0 mb-2">
            <p>
              {% if post.description %}
                {{ post.description }}
              {% else %}
                {{ post.content | strip_html | truncate: 120 }}
              {% endif %}
            </p>
          </div>

          <div class="post-meta flex-grow-1 d-flex align-items-end">
            <div class="me-auto">
              <i class="far fa-calendar fa-fw me-1"></i>
              {{ post.date | date: "%Y.%m.%d" }}
            </div>
          </div>
        </div>
      </div>
    </a>
  </article>
{% endfor %}

</div>