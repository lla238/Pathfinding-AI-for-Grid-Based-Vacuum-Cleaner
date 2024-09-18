# Overview
This project implements common search algorithms to navigate and optimize the pathfinding of a vacuum cleaner in a grid of rooms. The grid contains obstacles, walls, and dirty rooms that need to be cleaned by the AI agent. The goal is to efficiently move the agent through the grid using various search techniques to clean all dirty rooms with the least amount of movement and computational cost.

# Features
## Implement 5 Search Algorithms:

- **Breadth-First Search (BFS)**
  - Explores all possible rooms level by level from the starting position. This algorithm guarantees finding the shortest path in an unweighted grid but can be inefficient in terms of the number of rooms explored.
- **Depth-First Search (DFS)**
  - Explores as deep as possible into one path before backtracking. While it may find a solution, it doesn't guarantee the shortest path and often explores unnecessary rooms.
- **Uniform Cost Search (UCS)**
  - Similar to BFS, but takes into account the cost of moving between rooms. UCS ensures that the path with the lowest cumulative cost is found, making it optimal for grids with varying movement costs.
- **Greedy Best-First Search**
  - Focuses on moving towards the goal (a dirty room) based on the heuristic function (Manhattan or Euclidean distance). It prioritizes proximity to the goal but doesn't always find the shortest path.
- __A*__
  - Combines UCS and Greedy Search by using both the actual cost to reach a room and an estimate of the cost to reach the goal. A* is both optimal and efficient, finding the shortest path while minimizing the number of rooms explored.
## Heuristics:
- **Manhattan Distance**
  - A heuristic that calculates the total horizontal and vertical distance between the agent’s current position and the goal. This is useful in grids where movement is restricted to four directions (up, down, left, right) without diagonal movement.
- **Euclidean Distance**
  - Calculates the straight-line distance between two points. This heuristic is generally more accurate in environments where diagonal movement is possible or where precision is needed, though the difference from Manhattan distance is often minor in grid-based environments.
## Path cost optimization using step costs and penalties for turns.

## Optional behaviors: "StayLeft" and "StayTop" cost functions to influence the agent's path.

## Dynamic visualization of the agent’s path and explored rooms on the grid.
