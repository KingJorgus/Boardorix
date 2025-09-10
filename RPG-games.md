---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<div class="rpg-posts">
  {% assign rpg_posts = site.categories.RPG %}
  {% for post in rpg_posts %}
    <div class="rpg-card">
      <img src="{{ post.image | default: post.thumbnail | default: '/assets/images/default.png' }}" alt="{{ post.title }}" class="rpg-img"/>
      <h2>{{ post.title }}</h2>
      <p>{{ post.description }}</p>
      <a href="{{ post.url | relative_url }}" class="learn-more-btn">Learn More</a>
    </div>
  {% endfor %}
</div>
