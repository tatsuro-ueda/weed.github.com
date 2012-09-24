---
layout: post
category : "iOSlibrary"
tags : ["Podfile"]["cocoaPods"]
---
{% include JB/setup %}

## Podfileの書き方

{% highlight ruby %}
	platform :ios
	xcodeproj './MovieTimeline.xcodeproj'
	pod 'AFNetworking'
	pod 'LBGIFImage'
	pod 'ATMHud'
{% endhighlight %}