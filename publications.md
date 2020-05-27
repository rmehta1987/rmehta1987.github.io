---
layout: page
title: Publications
---

 testing

{% for post in site.publications %}

 {{post.ref-title}}
 {{post.title}}
 testing

{% endfor %}

{% for tips in site.tips %}
<h2><a href="{{ tips.url}}">{{ tips.title }}</a></h2>

{% endfor %}
