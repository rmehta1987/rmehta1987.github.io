---
layout: page
title: Publications
---

 testing

{% for post in site.publications %}

 <h2>{{post.ref-title}}</h2>
  <h2>{{post.title}}</h2>
 <h2>testing</h2>

{% endfor %}

{% for tips in site.tips %}
<h2><a href="{{ tips.url}}">{{ tips.title }}</a></h2>

{% endfor %}
