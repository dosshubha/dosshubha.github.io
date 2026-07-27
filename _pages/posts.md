---
title: "Posts"
permalink: /posts/
layout: single
author_profile: true
---

Here I write excerpts of my papers.

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url | relative_url }})

{% if post.excerpt %}
{{ post.excerpt }}
{% endif %}

<small>{{ post.date | date: "%B %d, %Y" }}</small>

---

{% endfor %}
