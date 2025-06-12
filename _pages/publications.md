---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if site.author.googlescholar %}
You can also find my articles on <u><a href="{{ site.author.googlescholar }}">Google Scholar</a></u>.
{% endif %}

## Journal Papers
<ul class="publication-list">
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'article' %}
      <li>{% include archive-single.html %}</li>
    {% endif %}
  {% endfor %}
</ul>

## Conference Papers
<ul class="publication-list">
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'inproceedings' %}
      <li>{% include archive-single.html %}</li>
    {% endif %}
  {% endfor %}
</ul>

## Posters
<ul class="publication-list">
  {% for post in site.publications reversed %}
    {% if post.pubtype == 'poster' %}
      <li>{% include archive-single.html %}</li>
    {% endif %}
  {% endfor %}
</ul>

<p class="last-updated">
  This page was last updated on: {{ page.date | date: "%B %d, %Y" }}
</p>
