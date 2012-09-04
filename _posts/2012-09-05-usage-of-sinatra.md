---
layout: post
category : Github
tags : ["GitHub Pages"]
---
{% include JB/setup %}

##Sinatraの使い方あれこれ

###異なるルートで同じ対応をしたい

DRYを実践したい

	require 'sinatra'
	
	['/one', '/two', /'three'].each do |route|
	  get rounte do
		"Triggered #{route} via GET"
	  end
	
	  post route do
		"Triggered #{route} via POST"
	  end
	end

###RESTリクエストのパラメータを受け取りたい
例えばこんなリクエスト

	http://my.server.address/function?key1=value1&key2=value2&key3=value3
	
こんなふうに受けることができる

	require 'sinatra'
	
	get '/function' do
  	  params['key1']
  	  params['key2']
  	  params['key3']
	end

###正規表現を用いたルート

	require 'sinatra'
	
	get %r{/(sp|gr)eedy} do
	  "You got cought in the greedy route!"
	end
	
###別のルートへリダイレクトする

	require 'sinatra'
	
	get '/redirect' do
	  redirect 'http://www.google.com'
	end
	
	get '/redirect2' do
	  redirect 'http://www.google.com', 301
	end

エラーコード301は「Moved Permanently」
デフォルトは302「Temporary redirection」

###静的なファイルを見せる

	require 'sinatra'
	
	get '/public.html' do
	end

`public`フォルダが使われる。例えば`public`フォルダの中に`javascrpts`フォルダがあるとすると、`http://localhost:4567/javascripts`でアクセスできる。

###Erbファイルを見せる

まず`views`フォルダを作る。

	require 'sinatra'
	
	get '/index' do
	  erb :index
	end

###Erbファイルに変数を渡す

	require '/home' do
	  @name = 'Random User'
	  erb :home
	end

インスタンス変数にアクセスする。

	<!DOCTYPE html>
	<html>
	<head>
	  <meta charset="UTF-8">
	  <title>Using variables</title>
	</head>
	<body>
	  <h1>Hello, <%= @name %>!</h1>
	</body>
	</html>

評価したい文は`<%= %>`タグで囲む。ループによる制御構造などは`<% %>`で囲む。

###事前・事後に処理したいことがあるとき

	require 'sinatra'
	
	before do
	  @before_value = 'foo'
	end
	
	get '/' do
	  "before_value has been set to #{@before_value}"
	end
	
	after do
	  puts "After Filter called to perform some task"
	end

"After Filter called to perform some task"はターミナルに出力される

###404 Not Foundのカスタマイズ

	require 'sinatra'
	
	before do
	  content_type :txt
	end
	
	not_found do
	  "Whoops! You requested a route that wasn't available."
	end

###500 Internal Server Errorのカスタマイズ

	require 'sinatra'
	
	…
	
	error do
	  "Y U NO WORK?"
	end

###Session管理

	require 'sinatra'
	
	configure do
	  enable :sessions
	end
	
	before do
	  content_type :txt
	end
	
	get '/set' do
	  session[:foo] = Time.now
	  "Session value set."
	end
	
	get '/fetch' do
	  "Session value: #{session[:foo]}"
	end

セッションをクリアするには

	get '/logout' do
	  session.clear
	  redirect 'fetch'
	end

###Cookieの利用

	require 'sinatra'
	
	get '/' do
	  response.set_cookie "foo", "bar"
	  "Cookie set. Would you like to <a href='/read'>read it</a>?"
	end
	
	get '/read'
	  "Cookie has a value of: #{request.cookies['foo']."
	end
	
	get '/delete'
	  response.delete_cookie "foo"
	  "Cookie has been deleted."
	end

###ファイル添付

	require 'sinatra'
	
	before do
	  content_type :txt
	end
	
	get '/attachment' do
	  attachment 'name_your_attachment.txt'
	  "Here's what will be sent downstream, in an attachment called 'name_your_attachment.txt'."
	end

