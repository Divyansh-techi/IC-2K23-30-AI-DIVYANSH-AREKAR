This repository contains five basic Artificial Intelligence search and navigation programs implemented in Python 3.

Programs Included

Maze Solver

Graph Traversal

Route Planning

Robot Navigation

8-Puzzle Solver

1. Maze Solver

Algorithm

Depth First Search (DFS) with Backtracking

Description

The maze contains:

S = Start

G = Goal

0 = Open path

1 = Wall

* = Final path

The program starts from S and recursively explores possible directions until it reaches G. If a direction does not lead to the goal, the algorithm backtracks.

AI Concept

State-space search and backtracking.

Complexity

Time: O(R × C)

Space: O(R × C)

2. Graph Traversal

Algorithms

Breadth First Search (BFS)

Depth First Search (DFS)

Description

The graph is represented using an adjacency list. The program traverses the graph starting from a selected node.

BFS

BFS uses a queue and explores nodes level by level.

DFS

DFS uses recursion (or a stack) and explores one branch as deeply as possible before backtracking.

AI Concept

Graph/state-space search.

Complexity

For V vertices and E edges:

BFS: O(V + E)

DFS: O(V + E)

3. Route Planning

Algorithm

Breadth First Search (BFS)

Description

Cities are represented as graph nodes and roads as edges. The program finds a route from a starting city to a destination city.

Because BFS explores the graph level by level, it finds a route with the minimum number of edges when all edges have equal cost.

AI Concept

Uninformed search and path finding.

Complexity

Time: O(V + E)

Space: O(V)

4. Robot Navigation

Algorithm

Breadth First Search (BFS)

Description

A robot moves through a grid from R (Robot) to G (Goal).

The robot can move:

Up

Down

Left

Right

Obstacles are represented by 1, while open cells are represented by 0.

The program searches for a valid path and marks the discovered path with *.

AI Concept

State-space search and path finding.

Complexity

For a grid with R rows and C columns:

Time: O(R × C)

Space: O(R × C)

5. 8-Puzzle Solver

Algorithm

A (A-Star) Search*

Description

The 8-puzzle consists of eight numbered tiles and one blank space represented by 0.

Example:

1 2 3
4 0 6
7 5 8

The goal state is:

1 2 3
4 5 6
7 8 0

The program uses A* search to find a sequence of moves from the initial state to the goal state.

A* Evaluation Function

f(n) = g(n) + h(n)

Where:

g(n) = cost from the initial state to the current state

h(n) = estimated cost from the current state to the goal

f(n) = estimated total cost

Heuristic Used

The program uses Manhattan Distance.

For every tile:

Manhattan Distance =
|current_row - goal_row| +
|current_column - goal_column|

The distances of all tiles are added to obtain h(n).

AI Concept

Informed search and heuristic search.

Complexity

The 8-puzzle has a finite state space, but A* can still require significant time and memory for difficult configurations. Its practical performance depends heavily on the heuristic.

Technologies Used

Python 3

collections.deque for BFS

heapq for A* priority queue

Python set for visited-state tracking

No external libraries are required.

How to Run

Make sure Python 3 is installed.

Run each program using:

python filename.py

For example:

python maze_solver.py

Suggested File Structure

AI-Practical/
│
├── maze_solver.py
├── graph_traversal.py
├── route_planning.py
├── robot_navigation.py
├── eight_puzzle.py
└── README.md

Quick Comparison

Program

Algorithm

Search Type

Main Purpose

Maze Solver

DFS

Uninformed

Find a path through a maze

Graph Traversal

BFS + DFS

Uninformed

Visit graph nodes

Route Planning

BFS

Uninformed

Find a route between cities

Robot Navigation

BFS

Uninformed

Navigate a grid

8-Puzzle Solver

A*

Informed

Solve a puzzle using a heuristic

Key AI Search Terms

State

A possible configuration of the problem.

Initial State

The starting configuration.

Goal State

The desired final configuration.

Action

A possible move from one state to another.

State Space

The collection of all possible states.

Search

The process of exploring states to reach the goal.

Heuristic

An estimate of the remaining cost from the current state to the goal.

Conclusion

These programs demonstrate fundamental AI search techniques:

DFS for maze solving

BFS and DFS for graph traversal

BFS for route planning

BFS for robot navigation

A* with Manhattan Distance for the 8-puzzle

Together, they provide examples of both uninformed search and informed/heuristic search in Artificial Intelligence.