---
layout: post
title: "find and replace in python"
date: 2013-07-13 22:51
comments: true
categories: python
---

{% codeblock find and replace lang: python %}
def find_replace(string, find, replace):
    len_find = len(find)
    len_replace = len(replace)
    st = string
    for i in range(len(string) - len(find) + 1):
        if string[i:i+len_find] == find:
            st = st[:i] + replace + st[i+len_find:]
    return st    

string = 'john'
find = 'n'
replace = 'nn'
print find_replace(string, find, replace)
{% endcodeblock %}

This program can find string of any length and replace it with any string. If you have any better program please put it in the comments.
Change the value of string if you want any custom string, similarly change the find and replace variables.