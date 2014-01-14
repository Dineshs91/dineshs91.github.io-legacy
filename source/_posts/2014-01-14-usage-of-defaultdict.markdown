---
layout: post
title: "Usage of defaultdict"
date: 2014-01-14 08:55
comments: true
categories: python
---

defaultdict is a built in function in python. It is available in collections package.

1.) 1st usage. If you want to know the frequency of characters in a word,

{% codeblock lang: python %}

from collections import defaultdict

a = “Amazon”
res = defaultdict(int)
for k in a:
    res[k] += 1
print res

{% endcodeblock %}

The result is {'A': 1, 'm': 1, 'a': 1, 'z': 1, 'o': 1, 'n': 1}
This program is case sensitive so it counts ‘A’ and ‘a’ seperately. If you want the program to be case insensitive just change to a.lower() in for loop.

{% codeblock lang: python %}

from collections import defaultdict

a = “Amazon”
res = defaultdict(int)
for k in a.lower():
    res[k] += 1
print res

{% endcodeblock %}

The result is {'a': 2, 'm': 1, 'z': 1, 'o': 1, 'n': 1}

2.) Using a list in defaultdict. 

{% codeblock lang: python %}

s = [(‘yellow’, 1), (‘blue’, 2), (‘yellow’, 3), (‘blue’, 4)]
d = defaultdict(list)
for k, v in s:
    d[k].append(v)

{% endcodeblock %}

The result is [('blue', [2, 4]), ('yellow', [1, 3])]
