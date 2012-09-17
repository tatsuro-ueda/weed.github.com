---
layout: post
category : "Heroku"
tags : ["Heroku"]["GitHub"]
---
{% include JB/setup %}

##GitHubとHerokuに両対応させるには

1. herokuでapp:create

		$ heroku apps:create p120902-jishiha-search
		Creating p120905-rss-process-test... done, stack is cedar
		http://p120905-rss-process-test.herokuapp.com/ | git@heroku.com:p120905-rss-process-test.git

2. `$ git clone https://github.com/weed/p120902-jishiha-search.git`
3. 作業
4. `$ git push heroku master`
5. ※ここでうまくいかないときは.git/configの`[remote "origin"]`を`[remote "heroku"]`に直したりすると、うまくいく
6. GitHubで空のレポジトリをつくる
7. .git/configに以下の記述を追加する

		[remote "origin"]	
			fetch = +refs/heads/*:refs/remotes/origin/*
			url = https://github.com/weed/p120902-jishiha-search.git

8. GitHub for Macで[repository]->[synclonize]で完了