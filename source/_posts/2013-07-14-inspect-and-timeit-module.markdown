---
layout: post
title: "Inspect and timeit module"
date: 2013-07-14 15:45
comments: true
categories: python
---
If you ever wondered how a certain function is implemented for ex: gcd(), there is just a module for this. If you want to have a look at the source of a module, you can do it in the following way.

{% codeblock Inspect a module lang: python %}
import inspect
from fractions import gcd
print inspect.getsource(gcd)
{% endcodeblock %}

gcd is used to find the greatest common divisor.
replace gcd with your own function.


If you want to find the execution time of a function, you can use the timeit module. A simple use of timeit module is shown below.

{% codeblock Timeit module lang: python http://docs.python.org/2/library/timeit.html python docs%}
def test():
    a = 0
    for i in range(100):
	a += i

if __name__ == "__main__":
    print (timeit.timeit("test()", setup="from __main__ import test", number=100))
{% endcodeblock %}

The output is the execution time in seconds.
For more on timeit module check the python docs.