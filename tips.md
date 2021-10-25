---
layout: default
title: Programming Thoughts
---

{% comment %}  
*
*  This loop loops through a collection called `collection_name`
*  and sorts it by the front matter variable `date` and than filters
*  the collection with `reverse` in reverse order
*
*  To make it work you first have to assign the data to a new string
*  called `sorted`.
*
{% endcomment %}

{% assign sorted = site.tips | sort: 'date' | reverse %}  
{% for tips in sorted %}
<h2><a href="{{ tips.url | prepend: site.baseurl }}">{{ tips.title }}</a></h2>

 <ul class="related-posts">
    <li>
        <h3>
          <small>{{ tips.description | truncate: 160 }}</small>
         </h3>
      </li>
  </ul>
{% endfor %}
