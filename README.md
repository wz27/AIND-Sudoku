# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

In this project, I expanded upon the Sudoku-solving agent developed in Udacity classroom lectures in order write an AI agent to solve Sudoku puzzles.

I wrote code to implement two extensions of our sudoku solver. The first one is to implement the technique called "naked twins". The second one is to modify our existing code to solve a diagonal sudoku.

The naked twins technique involves identifying a pair of boxes along the same column or row, both of which only permit the same 2 digits, and subsequently eliminating the 2 digits from the possible values of all other boxes along the same column or row.

A diagonal Sudoku puzzle is identical to traditional Sudoku puzzles with the added constraint that the boxes on the two main diagonals of the board must also contain the digits 1-9 in each cell (just like the rows, columns, and 3x3 blocks).

Below are the project instructions.

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: The naked twins technique applies the constraint that if two boxes that are in the same unit have the same two possibilities of digits, then those two digits are eliminated from the possibilities of every other box in the unit. The search space becomes smaller as it introduces new constraints for other boxes, reducing the number of possibilities.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: We create two new constraints in our solving algorithm, which are the two diagonal units in which no digit can appear more than once. Hence, we are still enforcing constraints to reduce the search space, but we carry out constraint propogation with two more constraints.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

