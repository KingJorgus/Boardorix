---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<section class="posts">
  {% assign rpg_posts = site.categories.RPG %}
  {% for post in rpg_posts %}
    <article class="post">
      {% if post.image %}
        <a href="{{ post.url | relative_url }}" class="post-image">
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
        </a>
      {% endif %}
      <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-description">{{ post.description }}</p>
      <a href="{{ post.url | relative_url }}" class="button primary">Learn More</a>
    </article>
  {% endfor %}
</section>
