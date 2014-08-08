---
layout: post
title: "Some useful tips for solving algorithm challenges"
date: 2014-08-05 22:26
comments: true
categories: algorithms
---

I’ve found some things useful, while solving challenges. I am sharing them with you.

The first and foremost thing, if you start coding as soon as you finish reading the 
problem, you will never get it right.

So the first tip:

1. Think first code later.
   Don’t even start coding if you don’t have a proper picture of the solution to the 
   problem.

2. Use appropriate names for your variables, functions and classes. This is important.
   This shows that you care about other programmers.

3. Try to find an efficient way of solving the problem at hand. Never settle with the
   solution you come up with first. Think again. 

4. If the problem involves numbers, think if sorting could help. Honestly, this 
   has helped me a lot of times. Sometimes you would have to come up with a different kind 
   of sorting. I will explain this with an example.

    Ex:
    Say you are inserting numbers in an array and after inserting, you’re solution needs
    sorting. There are two ways of doing it.

    Soln 1:
    You can first insert all the numbers and then sort.

    Soln 2:
    You can insert elements so that they are sorted. In python see bisect module.
    You do this by inserting the elements in the correct positions in the array, 
    so that after inserting, the array is sorted.

    Here soln 2 is efficient. 

5. If you’re stuck with a problem, look at it in a different perspective. It happens that,     
   you just think of the same thing, again and again. 


