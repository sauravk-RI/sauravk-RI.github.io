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

{% assign thesis_posts = site.publications | where: "pubtype", "phdthesis" %}
{% if thesis_posts.size > 0 %}
<h2 class="archive__item-title">Theses</h2>
{% for post in thesis_posts reversed %}
  {% include archive-single-publication.html %}
{% endfor %}
{% endif %}

{% assign book_posts = site.publications | where: "pubtype", "inbook" %}
{% if book_posts.size > 0 %}
<h2 class="archive__item-title">Book Chapters</h2>
{% for post in book_posts reversed %}
  {% include archive-single-publication.html %}
{% endfor %}
{% endif %}

{% assign journal_posts = site.publications | where: "pubtype", "article" %}
{% if journal_posts.size > 0 %}
<h2 class="archive__item-title">Peer-Reviewed Journal Papers</h2>
{% for post in journal_posts reversed %}
  {% include archive-single-publication.html %}
{% endfor %}
{% endif %}

{% assign conference_posts = site.publications | where: "pubtype", "inproceedings" %}
{% if conference_posts.size > 0 %}
<h2 class="archive__item-title">Peer-Reviewed Conference Papers</h2>
{% for post in conference_posts reversed %}
  {% include archive-single-publication.html %}
{% endfor %}
{% endif %}

{% assign patent_posts = site.publications | where: "pubtype", "patent" %}
{% if patent_posts.size > 0 %}
<h2 class="archive__item-title">Patents</h2>
{% for post in patent_posts reversed %}
  {% include archive-single-publication.html %}
{% endfor %}
{% endif %}