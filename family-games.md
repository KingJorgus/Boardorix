---
layout: page
title: Family Games
description: 'Reviews and recommendations for family games'
image: assets/images/family-games.png
order: 5
nav-menu: true
permalink: /family-games/
---

<div id="main" class="alt">

  <section id="one">
  <div class="inner">
  {% assign family_posts = site.categories.family %}
  {% for post in family_posts %}

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