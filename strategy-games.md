---
layout: page
title: Strategy Games
description: Reviews and recommendations for strategy games
image: assets/images/StrategyGames.jpg
order: 2
nav-menu: true
---

<div id="main" class="alt">

  <section id="one">
  <div class="inner">
  {% assign strategy_posts = site.categories.strategy %}
  {% for post in strategy_posts %}

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
