# Labryinth Solver


## Tasks


1) Generate a solvable random maze given the length and width as parameters

2) Solve the maze in the most efficient way possible

3) Draw the solution to the maze on top of the generated image

## Getting Started
## Software 
My implementation was fully in C++ and utilized the cmake platform for build automation and testing. The bulk of my algorithms are in my src folder.

## Installation and Usage

1. Clone the repo:
   ```sh
   git clone https://github.com/kazshah23/Labryinth-Solver.git
   ```
2. Make the `build` directory :
    ```sh
    mkdir build
    ```
3. Change directory into the `build` folder:
    ```sh
    cd build
    ```
4. In the `build` directory, "run cmake .."
   ```sh
   cmake ..
   ```
5. In the `build` directory, run make test && ./test to make sure all tests are passing
   ```sh
    make test && ./test
   ```
6. To see the output and breakdown of the code run make main && ./main  
    ```sh
   make main && ./main
    ```    
## Conclusions
1) To generating the maze, 
    - First created a function which takes in the length and width as parameters and intialized the maze as a grid, where each wall was set to true
    - Randomly deleted walls without creating cycles until I cannot delete anymore
    - See 'src/dsets.cpp' amd 'src/maze.cpp'
  
 2) To solve the maze,
    - Utilized Breath First Search (BFS) traversal in order to visit all the cells and keep track of distance from start
    - Located the cell with the longest distance and searched for the path to that cell
    - See 'src/maze.cpp'
  
 3) To draw the solution the maze
    - Call solvemaze in order to retrieve the solution to the maze 
    - Colored each pixel of the path red in order to illustrate a line path to the solution of the maze
 ## What I learned
 - The logic and applicability of Disjoint Sets
 - Generating images in C++ and drawing over them
 - Breath First Search (BFS) 
## Help

Any advise for common problems or issues.


## Authors

Contributors names and contact info

ex. Kazmain Shah
ex. [@kazshah23](kshah228@illinois.edu)
