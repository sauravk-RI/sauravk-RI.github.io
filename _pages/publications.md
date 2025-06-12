---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  You can also find my articles on <u><a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<!-- Check for Theses -->
{% for post in site.publications reversed %}
  {% if post.pubtype == 'phdthesis' %}
    {% assign has_thesis = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_thesis %}
## Theses
{% for post in site.publications reversed %}
  {% if post.pubtype == 'phdthesis' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
{% endif %}

<!-- Check for Book Chapters -->
{% for post in site.publications reversed %}
  {% if post.pubtype == 'inbook' %}
    {% assign has_books = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_books %}
## Book Chapters
{% for post in site.publications reversed %}
  {% if post.pubtype == 'inbook' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
{% endif %}

<!-- Check for Journal Articles -->
{% for post in site.publications reversed %}
  {% if post.pubtype == 'article' %}
    {% assign has_articles = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_articles %}
## Peer-Reviewed Journal Papers
{% for post in site.publications reversed %}
  {% if post.pubtype == 'article' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
{% endif %}

<!-- Check for Conference Papers -->
{% for post in site.publications reversed %}
  {% if post.pubtype == 'inproceedings' %}
    {% assign has_conferences = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_conferences %}
## Peer-Reviewed Conference Papers
{% for post in site.publications reversed %}
  {% if post.pubtype == 'inproceedings' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
{% endif %}

<!-- Check for Patents -->
{% for post in site.publications reversed %}
  {% if post.pubtype == 'patent' %}
    {% assign has_patents = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_patents %}
## Patents
{% for post in site.publications reversed %}
  {% if post.pubtype == 'patent' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
{% endif %}

<!-- Show uncategorized publications -->
{% assign has_uncategorized = false %}
{% for post in site.publications reversed %}
  {% unless post.pubtype %}
    {% assign has_uncategorized = true %}
    {% break %}
  {% endunless %}
{% endfor %}

{% if has_uncategorized %}
## Other Publications
{% for post in site.publications reversed %}
  {% unless post.pubtype %}
    {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endif %}