---
layout: page
title: Role Playing Games
description: Reviews and recommendations for role playing games.
image: assets/images/RPG.png
order: 4
nav-menu: true
permalink: /rpg-games/
---

h1>RPG Games</h1>

{% assign rpg_posts = site.categories.RPG | sort: 'date' | reverse %}
{% for post in rpg_posts %}
<article class="rpg-post">
  <h2>{{ post.title }}</h2>
  {{ post.content | markdownify }}
</article>
{% endfor %}

