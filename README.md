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

## Project Implementation 

In this project, based on the sudoku solving algorithm, I implemented two extended sudoku solving algorithm. The first extension is an implementation of the naked twins technique. The second is a modification of the algorithm to solve a diagonal sudoku.
1) Naked Twins Technique
![Test image](https://github.com/KHKANG36/Sudoku-Solving-Agent/blob/master/images/naked-twins1.png)
In the above image, 'F3' and 'I3' boxes are both belong to the same column and both permit the values of 2 and 3. Now, we don't know which one has a 2 and which one has a 3, but we know one thing for sure — the values 2 and 3 are locked in those two boxes, so no other box in their same unit (the third column) can contain the values 2 or 3.
Thus, we go over all the boxes in their same unit, and remove the values 2 and 3 from their possible values as below image
![Test image](https://github.com/KHKANG36/Sudoku-Solving-Agent/tree/master/images/naked-twins2.png)
As you can see, I have removed the values 2 and 3 from the boxes 'D3' and 'E3'. This is the naked twins technique. 
To implement this algorithm, I initially find the boxes which has the length of 2. Then, I searched the "peer boxes" which have the exact same digits of length 2. If we can find all common peers of "peer boxes" in sudoku board, we can remove the common digits of common peers because the digits should be locked to "peer boxes". Therefore, I finished to implement the Naked Twin algorithm by removing their common digits. 

2) Diagonal Sudoku 
A diagonal sudoku is like a regular sudoku, except that among the two main diagonals, the numbers 1 to 9 should all appear exactly once. 
![Test image](https://github.com/KHKANG36/Sudoku-Solving-Agent/tree/master/images/diagonal-sudoku.png)
This algorithm is just same as the regular sodoku. I just implemented diagonal units, and added it to whole unitlists. You can find the implementation between line #10 ~ #12 in my solution.py file. 

Below image is the result of running solution.py. Initially, it fills "123456789" in empty box, and then find the solutions based on the sudoku solving algorithm. The Naked Twins algorithm supports finding the solution more efficiently.
![Test image](https://github.com/KHKANG36/Sudoku-Solving-Agent/tree/master/images/Solution.png)









