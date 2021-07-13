---
title: Index
layout: post
---

4444---
{% assign iterateset = site.pages | where_exp:"item", "item.dir contains '/s/'" %}
{% for p in iterateset %}
<p><a href="{{p.url}}">{{p.title}}</a></p>
{% endfor %}
