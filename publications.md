---
layout: page
title: Publications
---

 testing

{% for post in site.publications %}

<li>
<h2><a href="{{ post.ref-url}}">{{ post.ref-title }}</a></h2>
  <a href="{% if post.ref-code %}{{ post.ref-code }}">[code]</a>
<\li>

{% endfor %}

