---
title: Index
layout: post
---

{% for p in site.pages | where_exp "item", "item.dir == '/s/'" %}
<p><a href="{{p.url}}">{{p.title}}</a></p>
{% endfor %}
