---
layout: page
title: Publications
---

{% assign sorted = (site.publications | sort: 'ref-year') | reverse %}
{% for post in sorted %}


<a href="{{ post.ref-url}}">{{ post.ref-title }}</a>  {% if post.ref-code != null %} <a href="{{post.ref-code}}">[Code]</a>  {% endif %}
{%- for author in post.ref-authors -%}
{%- if author contains "Mehta" -%}<b>{{author}}</b>{%- else -%}{{author}}{% endif %},&nbsp;
{%- endfor -%}  \n
{{post.ref-journal}}  
{%- endfor -%}

testing
