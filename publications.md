---
layout: page
title: Publications
---

{% assign sorted = (site.publications | sort: 'ref-year') | reverse %}
{% for post in sorted %}


{{ forloop.index }}. <a href="{{ post.ref-url}}">{{ post.ref-title }}</a>  {% if post.ref-code != null %} <a href="{{post.ref-code}}">Code</a>  {% endif %}
{% for author in post.ref-authors %}
{% if author contains "Rahul" %}**{{author}}**{% else %}{{author}}{% endif %}
{% endfor %}
{{post.ref-journal}}

    



{% endfor %}

