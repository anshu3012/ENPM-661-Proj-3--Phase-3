# ENPM-661-Proj-3--Phase-3-Group 38
## By Jaad Lepak, & Anshuman Singh

## Implementation of A* algorithm on a differential drive (non-holonomic) TurtleBot robot


In this project we will navigate a differential drive robot (TurtleBot 2 / TurtleBot 3) in a given map environment from a given start point to a given goal point, considering differential drive constraints while implementing the A* algorithm, with 8-connected action space.

## Dependencies
numpy 
matplotlib
math 

## Instructions to run 

 ## Program Explanation
 Searches fixed map to find optimal path from user-defined start and end
 Action set limited to 5 directions (0 deg, 30 deg, 60 deg, -30 deg, -60 deg)
 
 While searching, threshold of 0.5 used for X and Y directions and 30 degrees for angle
 
 The goal is determined reached when within 1.5 radius region of user-defined end coordinates
 
 After solution is found, map is displayed with:
    Obstacles in RED
    Explored vector paths in BLACK
    Goal region in GREEN
    Optimal path shown in BLUE
## Different sections of code:
### Libraries
  Imports all libraries
### User Inputs (Error-checking and robot dimensions)
  Error-checking functions
    Helps restrict inputs when asking user
  ### Robot radius and clearance
    User inputs for radius and clearance
### Map
  Generates the map using algebraic expressions to represent obstacles
### Obstacle Check
  Returns true if a point x,y is inside an obstacle
  Returns false if point is outside obstacle
### User Input (Coordinates)
  Collects start coordinates, end coordinates, step size, and starting angle
  Starting angle is input as degrees, then code converts to radians
  Requires user to re type in coordinate is inside obstacle
### Action Set
  Defines five actions sets relative to current x,y, and theta angle
    Move straight
    Up 30 degrees
    Up 60 degrees
    Down 30 degrees
    Down 60 degrees

## Node class and functions
  Functions to store node information and calculate total cost
## Generate graph
  Uses A star algorithm to iterate action sets throughout map
  Records visited vectors to plot
## Backtrack
  Plots a blue line on the optimal path
  
  
 

