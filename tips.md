---
layout: default
title: Programming Thoughts
---
{% assign tips_sorted = site.tips | sort: 'date' %}
{% for tips in tips_sorted %}
<h2><a href="{{ tips.url | prepend: site.baseurl }}">{{ tips.title }}</a></h2>

 <ul class="related-posts">
    <li>
        <h3>
          <small>{{ tips.description | truncate: 160 }}</small>
         </h3>
      </li>
  </ul>
{% endfor %}
