---
layout: post
title: "Exor sum of all non empty subsets in a list"
date: 2014-03-16 12:33
comments: true
categories: python
---

Consider one bit position at a time. How many of the terms have bit i set? The terms that have bit i set are exactly those that correspond to a subset that contains an odd number of inputs that have bit i set.

If there is any input that has bit i set, then exactly half of the 2N possible subsets will be of this form, and so they will contribute 2N−1+i to the final sum.

On the other hand, if no input has bit i set, then of course no terms will have that bit set either.

Summing these contributions of 2N−1+i per bit position is easy enough -- the final sum will simply be 2N−1 times the bitwise OR of all the inputs.

soon: (2 ** (N - 1)) * bitwise OR of all the inputs.
