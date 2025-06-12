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

<!-- Theses -->
{% assign thesis_posts = site.publications | where: "pubtype", "phdthesis" %}
{% if thesis_posts.size > 0 %}
## Theses
{% for post in thesis_posts reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

<!-- Book Chapters -->
{% assign book_posts = site.publications | where: "pubtype", "inbook" %}
{% if book_posts.size > 0 %}
## Book Chapters
{% for post in book_posts reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

<!-- Peer-Reviewed Journal Papers -->
{% assign journal_posts = site.publications | where: "pubtype", "article" %}
{% if journal_posts.size > 0 %}
## Peer-Reviewed Journal Papers
{% for post in journal_posts reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

<!-- Conference Papers -->
{% assign conference_posts = site.publications | where: "pubtype", "inproceedings" %}
{% if conference_posts.size > 0 %}
## Peer-Reviewed Conference Papers
{% for post in conference_posts reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

<!-- Patents -->
{% assign patent_posts = site.publications | where: "pubtype", "patent" %}
{% if patent_posts.size > 0 %}
## Patents
{% for post in patent_posts reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

<!-- Uncategorized Publications -->
{% assign uncategorized = site.publications | where_exp: "item", "item.pubtype == nil or item.pubtype == ''" %}
{% if uncategorized.size > 0 %}
## Other Publications
{% for post in uncategorized reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}