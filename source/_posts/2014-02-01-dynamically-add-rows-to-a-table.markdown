---
layout: post
title: "Dynamically add rows to a table"
date: 2014-02-01 00:28
comments: true
categories: jquery
---

If you want to dynamically add rows to an existing table use clone.

{% codeblock %}

tr = $(‘table tbody tr:last’).clone();
tr.appendTo($(‘table’));

{% endcodeblock %}

This adds rows at the bottom of the table.