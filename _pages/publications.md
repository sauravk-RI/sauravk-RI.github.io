layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
Debug Publications
Total publications found: {{ site.publications.size }}
Raw Publication List:
{% for post in site.publications %}

{{ post.title }} ({{ post.date | date: "%Y" }})

File: {{ post.path }}
Collection: {{ post.collection }}
{% endfor %}



Detailed Publication Info:
{% for post in site.publications %}
Title: {{ post.title }}
Date: {{ post.date }}
Venue: {{ post.venue }}
Collection: {{ post.collection }}
Permalink: {{ post.permalink }}
Publication Type: {{ post.pubtype }}
All fields: {{ post | jsonify }}
{% endfor %}