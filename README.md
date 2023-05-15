# 8-puzzle-game
The Eight Puzzle Game

Introduction: 
8 Puzzle problem is a classic problem of AI which can be solved by searching the solution space. This Project is given by Dr. Eamonn Keogh in the course of CS 205. We have to solve this problem using Uniform Cost Search, A* search with Misplaced Tiles Heuristic and Manhattan Distance Heuristic. I have implemented the code in the Python programming language to solve the problem and generated all the analyzing graphs using matplotlib pyplot.

8 puzzle problem:
8-puzzle problem has 9 cells (3*3) including one blank cell which is marked by 0. So there are 8 cells marked by 1 to 8 in the 3*3 boards. The goal of this problem is to convert the initial board to the solution state where we can have only certain moves from each placement. To be exact, we can move the blank cell either to the left or right or up or down if it is valid. The max depth of this problem is 31 and the branching factor is 4.

Initial state: <br>
1 2 3 <br>
5 6 4 <br>
0 8 7 <br>
Goal state:
1 2 3 <br>
4 5 6 <br>
7 8 0 <br>

Algorithms used to solve this problem:
Uniform Cost Search:
A* search with Misplaced Tiles Heuristic
A* search with Manhattan Distance Heuristic

Uniform Cost Search:
This algorithm works similarly to BFS where level of the nodes is counted as the original cost g(n) which is increased by 1 whenever the level is increased . So this algorithm searches the space level by level. It is also similar to A* search where h(n)=0.

A* search with Misplaced Tiles Heuristic:
A* search expands the nodes with the minimum f(n) where f(n) = g(n) + h(n), g(n) is the original cost from initial node to that node  and h(n) is the heuristic cost. g(n) is calculated as the level of the expanding node. But for h(n) we can use any good admissible heuristic. Here we will use misplaced tiles heuristic. An example is given below:


Initial state: <br>
1 2 3 <br>
5 6 4 <br>
0 7 8 <br>
Goal state:
1 2 3 <br>
4 5 6 <br>
7 8 0 <br>
Number of misplaced Tile (Excluding blank tile): 2
So, h(n) = 2
 
A* search with Manhattan Distance Heuristic:
This search also works just like the above but with a different heuristics, Manhattan Distance Heuristic.
Here h(n) = coordinate difference of each tile from current state to goal state.

Current state: <br>
1 2 3 <br>
4 0 6 <br>
7 8 5 <br>
Goal state:
1 2 3 <br>
4 5 6 <br>
7 8 0 <br>
Here, all cells are in place , only exception 5 which is on the wrong cell. 
So, h(n) = vertical distance and horizontal distance 
  = 1 + 1 = 2

