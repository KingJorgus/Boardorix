---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

<h1>RPG Games</h1>

{% for post in site.categories.RPG %}
  <article class="rpg-post">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.date | date: "%B %d, %Y" }}</p>
    {{ post.content }}
  </article>
{% endfor %}
