---
layout: post
title: "List comprehension"
date: 2013-07-23 11:12
comments: true
categories: python
---

List comprehensions are very useful. Here are some examples

1.) Get input and store it in a list

{% codeblock lang: python %}
>>> a = [raw_input() for _ in range(n)]
{% endcodeblock %}

Here 'n' is the number of elements. For example if you want to store 5 names then 'n' is 5.

2.) Convert numbers from a list which are stored in string to int

{% codeblock lang: python %}
>>> a = [int(i) for i in lis]
{% endcodeblock %}

Here 'lis' is the list which contains the numbers.

3.) If we want a multidimensional list

{% codeblock lang: python %}
>>> a = [ [0 for col in range(5)] for row in range(10)]
{% endcodeblock %}

This creates a multidimensional list containing 10 rows and 5 columns.

4.) Get the numbers greater than 100 from another list

{% codeblock lang: python %}
>>> a = [i for i in lis if i > 100]
{% endcodeblock %}

'lis' is the list which contains the numbers. The numbers in list 'lis' which are greater than 100 are added to list 'a'

5.) If you want to add a number to all the numbers in a list

{% codeblock lang: python %}
>>> a = [i+3 for i in lis]
{% endcodeblock %}

We are adding 3 to all the numbers in 'lis' and storing in 'a'. If you want to store it in 'lis' itself replace a with lis.