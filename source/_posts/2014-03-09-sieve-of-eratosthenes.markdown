---
layout: post
title: "Sieve of eratosthenes"
date: 2014-03-09 14:02
comments: true
categories: python
---

Sieve of eratosthenes is used to find the prime numbers.

{% codeblock %}
def sieve(limit):
    p = [True] * limit
    p[0] = p[1] = False
    for i, isprime in enumerate(p):
        if isprime:
            for n in xrange(i * i, limit, i):
                p[n] = False
    return p

p = sieve(100)
for i, j in enumerate(p):
    print i,’—>’,j
{% endcodeblock %}

sieve(100) - Has a list of first 100 numbers and whether they are prime or not.

Runtime: O(log log n)