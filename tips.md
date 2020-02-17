---
layout: default
title: Python and Matlab Tips
---

{% for tips in site.tips %}

<a href="{{ tips.url | prepend: site.baseurl }}"><h2>{{ tips.title }}</h2></a>
<p class="post-excerpt">{{ tips.description | truncate: 160 }}</p>

{% endfor %}
