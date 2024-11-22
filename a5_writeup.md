# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?
Depth-First algorithms are best in environments with clearly defined failure conditions, like sudoku. When wrong choices eliminate themselves quickly, depth first searches quickly focus in on the most promising path and see it through to completion. In other environments where wrong choices lead to slow and meandering dead ends, breadth first searches are probably better because they can cut through the noise by looking at every possibility and finding one that pans out.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?
The choice of data structure affects what order the searches test scenarios. Stack and Queue are the most generally useful structures for searches like this, but another design might also work, like one that uses some method of evaluating the position and chooses the most promising one regardless of what branch it is on.
3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?
For a larger sudoku grid, all that would be needed to upscale it would be to change the size variable and update how the subgrids work. The basic search algorithms can be used in other contexts as well, like playing other games or modeling real-world optimization problems.