---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

This is my publications page.

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}