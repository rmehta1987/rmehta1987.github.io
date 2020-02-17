---
layout: default
title: Python and Matlab Tips
---

{% for tips in site.tips %}
<h2><a href="{{ tips.url | prepend: site.baseurl }}">{{ tips.title }}</a></h2>

 <ul class="related-posts">
    <li>
        <h3>
          <span class="post-date">{{ tips.description | truncate: 160 }}</span>
           <small>{{ tips.date | date_to_string }}</small>
          </a>
        </h3>
      </li>
  </ul>
{% endfor %}
