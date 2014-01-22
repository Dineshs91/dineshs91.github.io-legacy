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

Strategy of DFS is to search deeper in the graph whenever possible.

DFS progresses by expanding the first child node of the search tree that appears and thus going deeper and deeper until a goal node is found, or until it hits a node that has no children. Then the search backtracks, returning to the most recent node it hasn’t finished exploring.

Advantages of DFS:

1. It is cheap on memory.
2. It can use recursion.
3. It is better when there are many solution nodes.

Performance parameters:

1. Completeness: Is algorithm guaranteed to find a solution if one exists.
2. Optimality: Whether the algorithm finds the optimal solution.
3. Time complexity: How long the algorithm takes the find the solution.
4. Space complexity: How much memory is needed.

Measuring complexity:

1. Branching factor(b): Maximum number of successors of any node.
2. Depth(m): Shallowest goal node in number of steps or levels.
3. Maximum depth: Maximum depth of the search tree.

Analysis:

Time: O(|V| + |E|)
Space: O(|V|)

Application:

Search problems in artificial intelligence.

Algorithm:

Visit a node, then push all of the nodes to be visited onto the stack. To find the next node to visit we simply pop a node of the stack, and then push all the nodes connected to that one onto the stack as well and we continue doing this until all nodes are visited.

There are 2 ways of doing this.

1. Using stack.



2. Using recursion.

DFS(v):
    visited[v] = 1
    for all w adjacent to v:
        if !visited:
            DFS(w)
