---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<section class="tiles">
  {% assign rpg_posts = site.categories.RPG %}
  {% for post in rpg_posts %}
    <article class="style2">
      <span class="image">
        {% if post.image %}
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" />
        {% else %}
          <img src="{{ '/assets/images/default.png' | relative_url }}" alt="No image available" />
        {% endif %}
      </span>
      <a href="{{ post.url | relative_url }}">
        <h2>{{ post.title }}</h2>
        <div class="content">
          <p>{{ post.description }}</p>
        </div>
      </a>
    </article>
  {% endfor %}
</section>
