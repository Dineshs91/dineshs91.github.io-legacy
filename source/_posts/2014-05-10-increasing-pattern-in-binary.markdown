---
layout: post
title: "Increasing pattern in binary"
date: 2014-05-10 11:57
comments: true
categories: algorithms
---

An useful trick which depends on the nature of binary numbers.

If we look at them, we can see the following pattern.

0, 1, 10, 11, 100, 101, 110, 111

We can see that they are in increasing order.
If we are interested in 2 digits, then this trick can come in very handy.
Take this example,

Find an integer X made up of 9's and 0's such that X is a multiple of N ?
X should contain 1 or more 9's and 0 or more 0's. 

So we could use our trick here.

Just replace 1 with '9'.

algorithm:
{% codeblock %}
    j = 1
    while str(bin(j)[2:]).replace('1','9')%n != 0:
        j += 1
    s = str(bin(j)[2:]).replace('1','9')
    print s
{% endcodeblock %}
This will give the least positive integer X made up of only 9's and 0's   