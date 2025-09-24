---
layout: page
title: Card Games
description: 'Reviews and recommendations for card games'
image: assets/images/card-games.png
order: 3
nav-menu: true
permalink: /card-games/
---

<div id="main" class="alt">

  <section id="one">
  <div class="inner">
  {% assign card_posts = site.categories.card %}
  {% for post in card_posts %}

  <header class="major">
   <h1>{{ post.title }}</h1>
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
