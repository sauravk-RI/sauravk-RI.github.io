---
layout: archive
title: "Videos"
permalink: /videos/
author_profile: true
---

{% for video in site.videos reversed %}
  <div class="archive__item">
    <h2 class="archive__item-title">{{ video.title }}</h2>
    {% if video.video_url %}
      <div class="archive__item-video">
        <iframe width="560" height="315"
          src="{{ video.video_url | replace: 'watch?v=', 'embed/' }}"
          frameborder="0" allowfullscreen></iframe>
      </div>
    {% endif %}
    {% if video.description %}
      <p>{{ video.description }}</p>
    {% endif %}
    <p class="archive__item-date"><em>{{ video.date | date: "%B %d, %Y" }}</em></p>
  </div>
{% endfor %}