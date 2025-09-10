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
        <a href="{{ post.url | relative_url }}" class="post-img">
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
        </a>
      {% else %}
        <a href="{{ post.url | relative_url }}" class="post-img">
          <img src="{{ '/assets/images/default.png' | relative_url }}" alt="No image available">
        </a>
      {% endif %}
      
      <header>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      </header>
      
      <p>{{ post.description }}</p>
      
      <footer>
        <a href="{{ post.url | relative_url }}" class="button primary">Learn More</a>
      </footer>
    </article>
  {% endfor %}
</section>
