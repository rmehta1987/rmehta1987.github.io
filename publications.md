---
layout: page
title: Publications
---


{% for post in site.publications %}

<li>
<h2><a href="{{ post.ref-url}}">{{ post.ref-title }}</a></h2>
 <a href="{if post.ref-code%}{{post.ref-code}}">Code</a>
</li>

{% endfor %}

