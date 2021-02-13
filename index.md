---
title: Index
layout: post
---

{% for p in site.pages | where "dir", "/s/" %}
<p><a href="{{p.url}}">{{p.title}}</a></p>
{% endfor %}
