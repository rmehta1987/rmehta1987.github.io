---
layout: page
title: Publications
---

{% assign sorted = (site.publications | sort: 'date') | reverse %}
{% for post in sorted %}


{{ forloop.index }}. <a href="{{ post.ref-url}}">{{ post.ref-title }}</a>  {% if post.ref-code != null %} <a href="{{post.ref-code}}">Code</a>  {% endif %}
{{post.ref-authors}}
{{post.ref-journal}}

    



{% endfor %}

