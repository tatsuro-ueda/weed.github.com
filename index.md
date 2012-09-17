---
layout: page
title: Weed.github.com
tagline: Supporting tagline
---
{% include JB/setup %}

## About this blog

This blog mainly introduce cocoaPods which is library of Objective-C.

このブログでは主にcocoaPodsというObjective-Cのライブラリを紹介します。

## Aoubt Me

![](http://farm9.staticflickr.com/8308/7976472200_f63eff2f59_o.jpg)

OSS project CocoaPod commiter. A free programmer mainly developed iOS application with Web service.

OSSプロジェクトのCocoaPodのコミッター。主にWebサービスをからめたiOSアプリの開発をしているフリーのプログラマです

### Contact

- [@weed_7777](https://twitter.com/weed_7777)
- <http://weed.github.com>
- weed_7777@yahoo.co.jp
- [weed's repositories](https://github.com/weed)
- [weed](http://stackoverflow.com/users/1530020/weed) @ StackOverflow

<!-- You also need to place a container where you'd like the Coderwall badges to render. -->
<section class="coderwall" data-coderwall-username="weed" data-coderwall-orientation="horizontal"></section>

## Old Blog

My old Blog is [here](http://weed.cocolog-nifty.com/wzero3es)

## iOS library list

The list is [here](https://github.com/weed/CocoaPods_selected/blob/master/pods.md)

## New Articles
### This part is under construction

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>