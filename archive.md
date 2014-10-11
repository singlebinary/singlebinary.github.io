---
layout: page
title: Archive
permalink: /archive/index.html
tags: [about, Jekyll, theme, responsive]
---

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}