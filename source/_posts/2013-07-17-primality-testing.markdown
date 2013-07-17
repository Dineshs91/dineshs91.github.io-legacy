---
layout: post
title: "Primality testing"
date: 2013-07-17 13:28
comments: true
categories: python
---
Here we are checking the prime numbers from 1 to 10**5. In both the methods we store the calculated prime numbers in a list and are used for calculating other prime numbers. I have used timeit module to check the execution time. The time is in seconds.

1. In the first method we use lists which contain the prime numbers that are calculated.
We divide the number(n) by prime numbers less than half of the number(n/2).

{% codeblock lang: python %}
from timeit import time

primeno = []

def prime(n):
  for i in xrange(2, n + 1):
    count = 0
    for j in primeno:
      if i % j == 0 and j <= (i/2)+1:
        count += 1
        break
    if count == 0:
      primeno.append(i)

start_time = time.time()
prime(10**5)
end_time = time.time()
total_time = end_time - start_time # Time in seconds
#print primeno
print 'Total time:', total_time
{% endcodeblock %}

2. In this method also we use lists but we divide the number(n) by the prime numbers which are less than the square root of the number(sqrt(n)).

{% codeblock lang: python %}
import math
from timeit import time

primeno = []

def prime(n):
    for i in xrange(2, n + 1):
        sq = math.sqrt(i)
        count = 0
        for j in primeno:
            if j > sq + 1:
                break
            if i % j == 0:
                count += 1
                break
        if count == 0:
            primeno.append(i)

start_time = time.time()
prime(10**5)
end_time = time.time()
total_time = end_time - start_time # Time in seconds
#print primeno
print 'Total time:', total_time


{% endcodeblock %}

Surely the second program runs faster. Run the program and see for yourself the difference in time between the two.
If you want the prime numbers just uncomment the line "#print primeno"
