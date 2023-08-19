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

## About my Project
To manage maze-related data, the code employs various data structures, including vectors, queues, and maps. Notably, it utilizes a disjoint set data structure (implemented as dsets) to track connected components and ensure maze connectivity without introducing cycles during generation. To solve the maze, the code utilizes Breadth-First Search (BFS) traversal, making use of queues, visited cell tracking, cell lengths, and path storage in maps.

The maze is represented as a grid of cells, with walls in four directions: up, down, left, and right, stored in the walls vector. The code also integrates functionality for generating visual representations of the maze using the cs225::PNG library. This includes setting up images, blackening specific edges to represent walls, and generating PNG images of both the maze and its solution. Importantly, when drawing the maze with a solution, the code highlights the path by changing the color of pixels along the route in the generated PNG image.

While the code lacks direct input functionality for specifying maze dimensions or other parameters, it provides a modular organization within a C++ class called SquareMaze, encapsulating maze generation, solving, and drawing functions. This modular structure enhances code clarity and ease of use. The introduction of randomness through the rand() function ensures that different mazes are generated each time the program runs, adding variety to the generated mazes. Overall, these technical features collectively enable the code to efficiently create, solve, and visually represent square mazes.
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
