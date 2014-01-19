---
layout: post
title: "DFS Demystified"
date: 2014-01-11 19:29
comments: true
categories: algorithms
---

Depth First Search (DFS).

A DFS explores a path all the way to a leaf before backtracking and exploring another path.

DFS always expands one of the nodes at the deepest level of the tree.
The search goes back once it hits a dead end.

Strategy of DFS is to search deeper in the graph whenever possible

Advantages of DFS:

1. It is cheap on memory.
2. It can use recursion.
3. It is better when there are many solution nodes.

Performance:

1. Completeness: Is algorithm guaranteed to find a solution if one exists.
2. Optimality: Whether the algorithm finds the optimal solution.
3. Time complexity: How long the algorithm takes the find the solution.
4. Space complexity: How much memory is needed.

Measuring complexity:

1. Branching factor(b): Maximum number of successors of any node.
2. Depth(m): Shallowest goal node in number of steps or levels.
3. Maximum depth: Maximum depth of the search tree.
