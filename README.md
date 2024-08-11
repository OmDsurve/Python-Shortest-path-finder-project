This project is a simple maze-solving application using Python's `curses` library. Here's a breakdown of its components and functionality:

Description:

Objective:**
The program displays a maze and uses a breadth-first search (BFS) algorithm to find the shortest path from a start point ('O') to an endpoint ('X'). The maze and the pathfinding process are visualized in the terminal using color and text.

Components:

1. Maze Representation:
   - The maze is represented as a 2D list where `"#"` denotes walls, `" "` denotes open spaces, `"O"` is the start point, and `"X"` is the endpoint.

2.Functions:
   - `print_maze(maze, stdscr, path=[])`: Displays the maze in the terminal. The path found by the BFS algorithm is highlighted in red.
   - `find_start(maze, start)`: Searches the maze to find the coordinates of the start point (`"O"`).
   - `find_path(maze, stdscr)`: Implements the BFS algorithm to find the shortest path from the start to the end. It updates the terminal display as it explores the maze.
   - `find_neighbors(maze, row, col)`: Determines the neighboring cells that can be moved to (up, down, left, right).

3. Terminal Display:
   - Uses `curses` to create a color-based terminal interface. Blue is used for the maze, and red is used for the path found by the BFS algorithm.

4. **Execution Flow:
   - `wrapper(main)`: Initializes the `curses` environment and starts the main function.
   - `main(stdscr)`: Sets up color pairs for terminal output and calls the `find_path` function to solve the maze.

 How It Works:
- The `find_path` function uses BFS to explore the maze. It starts from the `'O'` point and looks for the shortest path to the `'X'` point.
- As it explores, it updates the display to show the current state of the maze and the path being considered.
- Once the path is found, it is highlighted in red in the terminal.

 Usage:
- Run the script in a terminal that supports `curses` (e.g., Unix-based systems).
- The maze is displayed with the start point, walls, and endpoint. The BFS algorithm will find and show the shortest path in real-time.

This project serves as a practical example of using BFS for pathfinding and demonstrates how to use the `curses` library for simple graphical output in the terminal.
