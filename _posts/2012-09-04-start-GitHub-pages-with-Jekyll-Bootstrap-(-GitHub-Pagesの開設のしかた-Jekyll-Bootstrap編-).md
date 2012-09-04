---
layout: post
category : Github
tags : ["GitHub Pages"]
---
{% include JB/setup %}

##Start GitHub Pages with Jekyll Bootstrap by "GitHub for Mac" at September 2012


##GitHub Pagesの開設のしかた Jekyll-Bootstrap編（2012年9月版、なるべく「GitHub for Mac」を使う）

Jekyll-Bootstrap is the package that makes it easy to change Jekyll site into Blog. The feature of this is making it more easily than build with only Jekyll.

Jekyll-BootstrapはJekyllサイトを簡単にブログ化してくれるパッケージです。Jekyllだけで一から作るより手軽そうなのが特徴。

###English

1. create the repository named `USERNAME.github.com` in GitHub (You can left it blank).
2. clone **Jekyll-Bootstrap** into **local** folder named `USERNAME.github.com` by _GitHub for Mac_.
3. Edit `.git/config`

		[remote "origin"]
			fetch = +refs/heads/*:refs/remotes/origin/*
			url = git@github.com:USERNAME/USERNAME.github.com.git

	So now you can push the contents of `USERNAME.github.com` folder.
4. Publish by _GitHub for Mac_.
3. After minutes, the site is published. You can confirm the site by opening `http://USERNAME.github.com` with browser.
4. Next, edit `_config.yml` and change name, email address, Twitter account and others.
5. Commit & Sync by _GitHub for Mac_.
6. Let's try to write an post.

		$ vim _post/2012-03-22-installed-jekyll-bootstrap.md

5. Commit & Sync by _GitHub for Mac_.

###日本語

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
