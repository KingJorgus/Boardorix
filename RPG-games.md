---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<div class="section">
  {% assign rpg_posts = site.categories.RPG %}
  {% for post in rpg_posts %}
    <div class="rpg-card">
    <h2>{{ post.title }}</h2>
      {% if post.image %}
        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="post-img"/>
      {% else %}
        <img src="{{ '/assets/images/default.png' | relative_url }}" alt="No image available" class="post-img"/>
      {% endif %}
      <p>{{ post.description }}</p>
      <a href="{{ post.url | relative_url }}" class="button">Learn More</a>
    </div>
  {% endfor %}
</div>
