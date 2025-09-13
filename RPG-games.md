---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<div id="main" class="alt">

  <section id="one">
  <div class="inner">
  {% assign rpg_posts = site.categories.RPG %}
  {% for post in rpg_posts %}

  <header class="major">
   <h1>{{ page.title }}</h1>
  </header>
      {% if post.image %}
        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="post-img"/>
      {% else %}
        <img src="{{ '/assets/images/default.png' | relative_url }}" alt="No image available" class="post-img"/>
      {% endif %}
      <p>{{ post.description }}</p>
      <a href="{{ post.url | relative_url }}" class="button">Learn More</a>
  {% endfor %}
  </div>
</section>
</div>
