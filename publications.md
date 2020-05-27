---
layout: page
title: Publications
---


{% for post in site.publications %}

<li>
<h2><a href="{{ post.ref-url}}">{{ post.ref-title }}</a></h2>
 {% if post.ref-code != null %} 
    <a href="{{post.ref-code}}">Code</a>
  {% endif %}
</li>

{% endfor %}

