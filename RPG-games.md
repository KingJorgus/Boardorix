---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<section>
  <div class="posts">
    {% assign rpg_posts = site.categories.RPG %}
    {% for post in rpg_posts %}
      <article>
        <header>
          <h2>
            <a href="{{ post.url | relative_url }}">
              {{ post.title }}
            </a>
          </h2>
        </header>
        {% if post.image %}
          <a href="{{ post.url | relative_url }}" class="image fit">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" />
          </a>
        {% else %}
          <a href="{{ post.url | relative_url }}" class="image fit">
            <img src="{{ '/assets/images/default.png' | relative_url }}" alt="No image available" />
          </a>
        {% endif %}
        <p>{{ post.description }}</p>
        <ul class="actions">
          <li><a href="{{ post.url | relative_url }}" class="button">Learn More</a></li>
        </ul>
      </article>
    {% endfor %}
  </div>
</section>
