# Unit 1 – AI Problem Formulation & Intelligent Problem Solving

## Laboratory Activities

This folder contains Python implementations of four important Artificial Intelligence problem-solving techniques:

1. **Water Jug Problem**
2. **Missionaries and Cannibals Problem**
3. **Vacuum Cleaner Problem**
4. **State Space Representation using 8-Puzzle**

These programs demonstrate fundamental AI concepts such as **state-space representation, search, goal states, operators, constraints, and intelligent agents**.

---

# 1. Water Jug Problem

## Description

The Water Jug Problem is a classic **state-space search problem** in Artificial Intelligence.

We have two water jugs:

- Jug A → Capacity = 4 litres
- Jug B → Capacity = 3 litres

Initially, both jugs are empty.

The objective is to measure exactly **2 litres of water**.

## Allowed Operations

The following operations are allowed:

- Fill Jug A
- Fill Jug B
- Empty Jug A
- Empty Jug B
- Pour Jug A into Jug B
- Pour Jug B into Jug A

## State Representation

A state is represented as:

```text
(A, B)
```

where:

- `A` = amount of water in Jug A
- `B` = amount of water in Jug B

Example:

```text
(4, 2)
```

means Jug A contains 4 litres and Jug B contains 2 litres.

## Initial State

```text
(0, 0)
```

## Goal State

The goal is to have exactly 2 litres in either jug.

For example:

```text
(0, 2)
```

## Algorithm Used

**Breadth First Search (BFS)** is used to find a solution.

## Run

```bash
python water_jug.py
```

## AI Concepts

- State Space
- Initial State
- Goal State
- Operators
- Breadth First Search
- State Transition

---

# 2. Missionaries and Cannibals Problem

## Description

The Missionaries and Cannibals problem is a classic AI **state-space search and constraint satisfaction problem**.

There are:

- 3 Missionaries
- 3 Cannibals
- 1 Boat

The objective is to move everyone from the left bank to the right bank safely.

## Rules

1. The boat can carry a maximum of 2 people.
2. At least one person must be in the boat.
3. On either bank, if missionaries are present, cannibals must not outnumber missionaries.
4. Everyone must safely cross the river.

## State Representation

A state is represented as:

```text
(M, C, B)
```

where:

- `M` = Missionaries on the left side
- `C` = Cannibals on the left side
- `B` = Boat position

```text
0 = Left
1 = Right
```

Example:

```text
(3, 3, 0)
```

means:

- 3 missionaries on left
- 3 cannibals on left
- boat is on left

## Initial State

```text
(3, 3, 0)
```

## Goal State

```text
(0, 0, 1)
```

This means everyone has moved to the right side.

## Algorithm Used

**Breadth First Search (BFS)** is used.

Invalid states are rejected using the problem constraints.

## Run

```bash
python missionaries_cannibals.py
```

## AI Concepts

- State Space Representation
- Constraint Checking
- Breadth First Search
- Goal Testing
- State Transition
- Problem Solving

---

# 3. Vacuum Cleaner Problem

## Description

The Vacuum Cleaner Problem is a classic example of an **intelligent agent** and **state-space problem**.

There are two rooms:

```text
Room A
Room B
```

Each room can either be:

```text
Clean
Dirty
```

The vacuum cleaner must clean all dirty rooms.

## Possible Actions

The vacuum cleaner can:

- Move Left
- Move Right
- Suck dirt

## State Representation

A state can be represented as:

```text
(Location, A, B)
```

where:

- `Location` = current position of vacuum cleaner
- `A` = condition of Room A
- `B` = condition of Room B

Example:

```text
(A, Dirty, Clean)
```

means:

- Vacuum is in Room A
- Room A is dirty
- Room B is clean

## Initial State

The initial state depends on the input provided by the user.

Example:

```text
(A, Dirty, Dirty)
```

## Goal State

```text
(A, Clean, Clean)
```

or:

```text
(B, Clean, Clean)
```

The important condition is:

```text
Room A = Clean
Room B = Clean
```

## Basic Rules

```text
IF current room is Dirty
THEN Suck

IF current room is Clean
AND other room is Dirty
THEN Move to other room
```

## Run

```bash
python vacuum_cleaner.py
```

## AI Concepts

- Intelligent Agent
- Environment
- Perception
- Action
- State Representation
- Goal State
- Simple Reflex Agent

---

# 4. State Space Representation – 8 Puzzle

## Description

The 8-Puzzle is used to demonstrate **state-space representation** in Artificial Intelligence.

The puzzle consists of:

- 8 numbered tiles
- 1 blank space

Example:

```text
1 2 3
4 0 6
7 5 8
```

Here `0` represents the blank space.

## Objective

Move the tiles until the puzzle reaches the goal state:

```text
1 2 3
4 5 6
7 8 0
```

## State Representation

The complete puzzle configuration represents one state.

Example:

```text
(1, 2, 3,
 4, 0, 6,
 7, 5, 8)
```

## Operators

The blank space can move:

- Up
- Down
- Left
- Right

depending on its current position.

## Example

If the blank is in the center:

```text
1 2 3
4 0 6
7 5 8
```

possible movements include:

```text
Move Up
Move Down
Move Left
Move Right
```

## Initial State

```text
1 2 3
4 0 6
7 5 8
```

## Goal State

```text
1 2 3
4 5 6
7 8 0
```

## Run

```bash
python state_space.py
```

## AI Concepts

- State Space
- Initial State
- Goal State
- Operators
- State Transitions
- Search Space
- Problem Formulation

---

# Installation & Requirements

## Python

Make sure Python 3.x is installed.

Check the Python version:

```bash
python --version
```

or:

```bash
python3 --version
```

No external libraries are required for the basic programs except Python's built-in `collections` module.

---

# Project Structure

Recommended folder structure:

```text
AI_Unit_1_Lab/
│
├── README.md
│
├── water_jug.py
│
├── missionaries_cannibals.py
│
├── vacuum_cleaner.py
│
└── state_space.py
```

---

# How to Run

Open the terminal inside the project folder.

## Water Jug

```bash
python water_jug.py
```

## Missionaries and Cannibals

```bash
python missionaries_cannibals.py
```

## Vacuum Cleaner

```bash
python vacuum_cleaner.py
```

## State Space Representation

```bash
python state_space.py
```

---

# Comparison of the Four Problems

| Problem | Main Concept | State Representation | Main Technique |
|---|---|---|---|
| Water Jug | State Space Search | `(A, B)` | BFS |
| Missionaries & Cannibals | Search + Constraints | `(M, C, B)` | BFS |
| Vacuum Cleaner | Intelligent Agent | `(Location, A, B)` | Rule-based actions |
| 8-Puzzle | State Space Representation | Puzzle configuration | State transitions |

---

# Important AI Terminology

## State

A particular configuration of the problem.

Example:

```text
(4, 2)
```

in the Water Jug problem.

## Initial State

The starting point of the problem.

Example:

```text
(0, 0)
```

## Goal State

The desired final state.

Example:

```text
(0, 2)
```

## Operator

An action that transforms one state into another.

Examples:

```text
Fill Jug
Empty Jug
Pour Jug A → Jug B
```

## State Space

The complete set of possible states that can be reached from the initial state.

## Search

The process of exploring the state space to find a path from the initial state to the goal state.

## Breadth First Search

BFS explores states level by level and can find the shortest solution when all actions have equal cost.

## Constraint

A condition that must be satisfied for a state to be valid.

---

# Learning Outcomes

After completing these four practicals, we should be able to:

- Formulate AI problems using **states and operators**.
- Identify **initial and goal states**.
- Represent problems using **state-space representation**.
- Apply **Breadth First Search** to solve AI problems.
- Handle **constraints** during problem solving.
- Understand the basic working of an **intelligent agent**.
- Implement simple **rule-based actions** in Python.
- Understand how AI searches through possible states to reach a goal.

---

# Conclusion

These four laboratory activities provide the foundation for **AI problem formulation and intelligent problem solving**.

The **Water Jug** and **Missionaries & Cannibals** problems demonstrate search and state-space techniques. The **Vacuum Cleaner** demonstrates the concept of an intelligent agent, while the **8-Puzzle** demonstrates how an AI problem can be formally represented using states, operators, and goal conditions.

Together, these practicals provide a basic understanding of how Artificial Intelligence systems formulate problems and search for solutions.
