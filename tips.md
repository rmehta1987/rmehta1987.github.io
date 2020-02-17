---
layout: default
title: Python and Matlab Tips
---

{% for tips in site.tips %}

<h2><a href="{{ tips.url | prepend: site.baseurl }}">{{ tips.title }}</a></h2>
<span class="post-excerpt">{{ tips.description | truncate: 160 }}</span>
<span class="post-date">{{ tips.date | date_to_string }}</span>
<p></p>
{% endfor %}
