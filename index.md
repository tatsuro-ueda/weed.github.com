---
layout: page
title: Weed.github.com
tagline: Supporting tagline
---
{% include JB/setup %}

## Aoubt this blog

This blog mainly introduce cocoaPods which is library of Objective-C.

このブログでは主にcocoaPodsというObjective-Cのライブラリを紹介します。

## Aoubt Me

![](http://farm9.staticflickr.com/8308/7976472200_f63eff2f59_o.jpg)

A free programmer mainly developed iOS application with Network Web service.

主にネットワークのWebサービスをからめたiOSアプリの開発をしているフリーのプログラマです

### Contact

- [@weed_7777](https://twitter.com/weed_7777)
- <http://weed.github.com>
- <mailto:weed_7777@yahoo.co.jp>
- [weed](http://stackoverflow.com/users/1530020/weed) @ ![](http://farm9.staticflickr.com/8438/7976623292_85f2420bbd_t.jpg)

## Articles

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Old Blog

My old Blog is [here](http://weed.cocolog-nifty.com/wzero3es)