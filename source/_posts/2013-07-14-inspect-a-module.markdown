---
layout: post
title: "Inspect a module"
date: 2013-07-14 15:45
comments: true
categories: python
---

If you want to have a look at the source of a module, you can do this in the following way.

{% codeblock Inspect a module lang: python %}
import inspect
from fractions import gcd
print inspect.getsource(gcd)
{% endcodeblock %}

gcd is used to find the greatest common divisor.

Use the timeit module to view the running time.

{% codeblock Timeit module lang: python http://docs.python.org/2/library/timeit.html python docs%}
def test():
    a = 0
    for i in range(100):
	a += i

if __name__ == "__main__":
    print (timeit.timeit("test()", setup="from __main__ import test", number=100))
{% endcodeblock %}

The output is the execution time in seconds