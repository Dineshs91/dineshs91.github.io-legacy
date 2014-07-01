---
layout: post
title: "Check dependencies"
date: 2014-06-15 16:01
comments: true
categories: python
---

I have seen a lot of projects on github. Almost all of them, just specify the external packages required
for that project. The bad thing about dependencies is that, it's not enough if you just have that package,
but you should have a version that the project uses.

Let's take a scenario to understand this better:

Let's say there is a project 'Ringo' in github. I as a developer, decide to contribute to this project.
The first thing I will do is, fork that project. Then I clone it to my laptop. The next step, I will run
the test cases to check if everything works. But before, I have to get all of the dependencies. I have to
check all of the libraries, whether they are there or do I have to update. After checking, I install the 
missing dependencies manually. 

what if there are a lot of dependencies ? Now checking each one becomes tedious.

What i suggest:

Create a file, which when executed checks for all the dependencies present in your laptop and displays which
dependencies you have and which dependencies(with version no.) you need to install.

Advantage:

Let's consider the previous scenario again. After I clone the project to my laptop, the next step I will
do is, to run the check_dependencies.py file. It displays what versions of dependencies I have and what are
actually needed for that project. This reduces the manual checking part. I just have to install the 
dependencies that do not match the version used by the project.

You can think that, the projects have a requirements.txt file, is that not sufficient.
Yes it is sufficient. That is just a text file. But my idea, is more than just text. It can have logic. 

Think about this.

In requirements.txt there is a dependency on python-2.7 and I have python-2.6 in my system. The project will also work for python-2.6. But in requirements they cannot specify 
that.

So if you do $ pip install -r requirements.txt

you end up installing python-2.7 even though you can work on python-2.6
I am just taking the same concept to the next level.