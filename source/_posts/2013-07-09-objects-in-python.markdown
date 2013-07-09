---
layout: post
title: "objects in python"
date: 2013-07-09 11:37
comments: true
categories: python
---

Objects are used to access the methods of a class. Take a look at the following code.

{% codeblock objects in python lang: python %}

class Students(object):
  def __init__(self, name, no):
    self.name = name
    self.no = no

  def display(self):
    print 'Student name: %s and no: %d' %(self.name, self.no)

student1 = Students('mike', 15)
student1.display()

{% endcodeblock %}

In this code student1 is the object. __init__ is like constructor in c which is used to initialise the data. The name self holds the object itself. In this code 'self' is the object student1. You can create as many objects as you like.