---
layout: post
title: "using modular arithmetic"
date: 2013-07-20 11:13
comments: true
categories: python
---

Using modular arithmetic for various purposes.(In python)

1. If you want the decimal part of a number use mod operator.

>>> pi = 3.14159

>>> pi % 1
    .14159

2. If you want the digit in one's place and the most significant digit.

>>> a = 12

>>> a % 10
    2

>>> a / 10
    1


