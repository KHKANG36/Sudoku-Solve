# Solve Sudoku with AI

## Synopsis

In this project, I implemented Sudoku-solving agent lectured in the Udacity AI nanodegree program. This Sudoku-solving agent includes the diagonal-Sudoku solving technique and Naked twin technique, which are helper algorithms to resolve the Sudoku problem more efficiently.   

## Instructions

You need to configure the AIND environment
 - Setup the [Anaconda](https://www.continuum.io/downloads) environment.
 - Setup the AIND environment : Download the `aind-universal.yml` file in this repository. Open a terminal and run `conda env create -f aind-universal.yml` to create the environment.

## Start Guide

### Activate the aind environment (OS X or Unix/Linux)
    
    `$ source activate aind`

### Activate the aind environment (Windows)

    `> activate aind`

### Run the code & visualization

    `(aind)$ python solution.py`

## Algorithm

You must complete the required functions in the 'solution.py' file (copy in code from the classroom where indicated, and add or extend with new code as described below). The `test_solution.py` file includes a few unit tests for local testing (See the unittest module for information on getting started.), but the primary mechanism for testing your code is the Udacity Project Assistant command line utility described in the next section.

1. Add the two new diagonal units to the `unitlist` at the top of solution.py. Re-run the local tests with `python -m unittest` to confirm your solution. 

1. Copy your code from the classroom for the `eliminate()`, `only_choice()`, `reduce_puzzle()`, and `search()` into the corresponding functions in the `solution.py` file.

1. Implement the `naked_twins()` function, and update `reduce_puzzle()` to call it (along with the other existing strategies). Re-run the local tests with `python -m unittest -v` to confirm your solution.

1. Write your own test cases to further test your code. Re-run the remote tests with `udacity submit` to confirm your solution. If any of the remote test cases fail, use the feedback to write new local test cases that you can use for debugging.








