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
      {% if post.image %}
        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="rpg-img"/>
      {% else %}
        <img src="{{ '/assets/images/default.png' | relative_url }}" alt="No image available" class="rpg-img"/>
      {% endif %}
      <h2>{{ post.title }}</h2>
      <p>{{ post.description }}</p>
      <a href="{{ post.url | relative_url }}" class="learn-more-btn">Learn More</a>
    </div>
  {% endfor %}
</div>
