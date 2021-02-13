---
title: Index
layout: post
---

{% for p in site.pages | where "folder", "s" %}
<p><a href="{{p.url}}">{{p.title}}</a></p>
{% endfor %}
