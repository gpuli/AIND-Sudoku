# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In the naked twins problem, we check for two blocks that have the same value of length 2. We then check each of their peers and make a list of their overlap. Once we have a list of these overlaps, we iterate through this list and eliminate all the values that are repeated in the naked twins. This is because since the naked twins have only two values, they have to be present in the two blocks itself. Using this logic we can safely eliminate these values from their common peers and narrow down the possible values. As we keep doing this for the whole puzzle, this constraint is echoed in other places and propagates itself around the whole puzzle eventually giving us the solution.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: In the diagonal sudoku problem, we add a diagonal unit for the two criss-crossing diagonals. When we do this, for all the blocks that are located on these diagonals, we can eliminate from its diagonal peers all those values that are being repeated. Doing so, propagates the constraints to other areas of the puzzle as well eventually solving the entire puzzle. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project.
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.
