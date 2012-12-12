---
layout: page
title: Weed.github.com
tagline: Supporting tagline
---
{% include JB/setup %}

## Aoubt Me

![](http://farm9.staticflickr.com/8308/7976472200_f63eff2f59_o.jpg)

OSS project CocoaPod commiter. A free programmer mainly developed iOS application with Web service.

主にWebサービスをからめたiOSアプリの開発をしているフリーのプログラマです

### Contact

- [@weed_7777](https://twitter.com/weed_7777)
- <http://weed.github.com> (This page)
- weed_7777@yahoo.co.jp
- [weed's repositories](https://github.com/weed) @GitHub
- [weed](http://stackoverflow.com/users/1530020/weed) @StackOverflow
- [weed](http://coderwall.com/weed) @coderwall
- [weed](http://qiita.com/users/weed@github) @Qiita

<!-- You also need to place a container where you'd like the Coderwall badges to render. -->
<section class="coderwall" data-coderwall-username="weed" data-coderwall-orientation="horizontal"></section>

## Old Blog

My old Blog is [here](http://weed.cocolog-nifty.com/wzero3es)

## iOS library list

The list is [here](https://github.com/weed/CocoaPods_selected/blob/master/pods.md)

### Recent Updates

<script src='http://gitlive.com/githublive.min.js'></script>
<script>var GithubPush = {num_old:5,nodes:['weed/CocoaPods_selected']}</script>
<div id='commits'></div>

## New Articles
### This part is under construction

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>