---
layout: home
title: Home
---

# Latest Posts

{% assign posts_sorted = site.posts | sort: "date" | reverse %}
{% for post in posts_sorted %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
