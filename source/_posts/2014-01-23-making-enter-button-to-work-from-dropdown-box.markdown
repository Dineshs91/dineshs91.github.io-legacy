---
layout: post
title: "Making enter button to work from dropdown box"
date: 2014-01-23 22:00
comments: true
categories: jquery
---

{% codeblock lang: javascript %}

$(‘select’).live(‘key press’, function(e){
    if(e.which == 13){
	$(‘form’).submit();
    }
});

{% endcodeblock %}

