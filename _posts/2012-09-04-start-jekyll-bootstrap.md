---
layout: post
category : Github
tags : ["GitHub Pages"]
---
{% include JB/setup %}

##GitHub Pagesの開設のしかた Jekyll-Bootstrap編（2012年9月版）

Jekyll-BootstrapはJekyllサイトを簡単にブログ化してくれるパッケージです。Jekyllだけで一から作るより手軽そうなのが特徴。

1. `USERNAME.github.com`という名前のリポジトリをGitHubにつくる（空のままで良い）
2. _GitHub for Mac_で**Jekyll-Bootstrap**を**ローカルの**`USERNAME.github.com`というフォルダにcloneする
3. `.git/config`を編集する

		[remote "origin"]
			fetch = +refs/heads/*:refs/remotes/origin/*
			url = git@github.com:USERNAME/USERNAME.github.com.git

	これで、先ほど作った空のリポジトリに`USERNAME.github.com`フォルダの中身をPushできる。
4. _GitHub for Mac_でPublishする
3. しばらく待つとサイトができるので、`http://USERNAME.github.com`をブラウザで開いて確認する
4. 次に`_config.yml`を編集して名前やらメールアドレスやらTwitterアカウントを編集する
5. _GitHub for Mac_でCommit & Syncする
6. 記事を書いてみる

		$ vim _post/2012-03-22-installed-jekyll-bootstrap.md

5. _GitHub for Mac_でCommit & Syncする
