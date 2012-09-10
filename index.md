---
layout: page
title: Weed.GitHub.com
tagline: Supporting tagline
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Old Blog

My old Blog is [here](http://weed.cocolog-nifty.com/wzero3es)