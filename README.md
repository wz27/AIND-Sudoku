# Sudoku project details

## Synopsis

In this project, I expanded upon the Sudoku-solving agent developed in Udacity classroom lectures in order write an AI agent to solve Sudoku puzzles. 

I wrote code to implement two extensions of our sudoku solver. The first one is to implement the technique called "naked twins". The second one is to modify our existing code to solve a diagonal sudoku. 

The naked twins technique involves identifying a pair of boxes along the same column or row, both of which only permit the same 2 digits, and subsequently eliminating the 2 digits from the possible values of all other boxes along the same column or row.

A diagonal Sudoku puzzle is identical to traditional Sudoku puzzles with the added constraint that the boxes on the two main diagonals of the board must also contain the digits 1-9 in each cell (just like the rows, columns, and 3x3 blocks).
