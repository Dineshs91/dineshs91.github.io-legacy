---
layout: post
title: "Fibonacci number"
date: 2014-01-31 23:59
comments: true
categories: algorithms
---

A number is a fibonacci number if 5*N2 +- 4 is a perfect square. sqrt(r1) % 1 == 0. This is for checking if the number is a perfect square.

r1 = sqrt(5*n**2+4)
r2 = sqrt(5*n**2-4)
isSquare = r1 % 1 == 0 or r2 % 1 == 0
if(isSquare):
    print “isFibo”