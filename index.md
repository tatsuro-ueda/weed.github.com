---
layout: page
title: Weed.github.com
tagline: Supporting tagline
---
{% include JB/setup %}

## Aoubt this blog

This blog mainly introduce cocoaPods which is library of Objective-C.

## Aoubt Me

A free programmer mainly developed iOS application with Network Web service.

## Artivles

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Old Blog

My old Blog is [here](http://weed.cocolog-nifty.com/wzero3es)