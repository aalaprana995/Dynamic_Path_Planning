# Multiple_Robot_with_PRM

Motion planning project for multiple robot system using PRM for static and dynamic obstacles.

## Introduction

- Motion planning is a term used in robotics for the process of breaking down a desired movement task into discrete motions that satisfy movement constraints and possibly optimize some aspect of the
movement.
- There are two main kind of obstacles in planning which are namely static obstacles and dynamic obstacles. As the
name suggests that static obstacles have a fixed position and orientation in configuration space which does
not vary with time,in contrast to dynamic obstacles.

This project aims to find an optimal solution to the planning problem which has both static and
dynamic obstacle in the environment with no constraints in movements, provided we have prior knowledge
about the initial position of the obstacles.

## Assumptions
- There is a upper bound on the velocity of the robot.
- There is no constraints on shape and motion of dynamic obstacles as long as we have prior knowledge
of its motions.
- There is no restriction on robot’s motion.
- The road map for static obstacles is computed in prepossessing phase without time as a parameter.

##  Algorithm
Probabilistic road-map planner (PRM) algorithm is used for finding the feasible path. 
- The main principle behind PRM algorithm is that it takes random samples
from the configuration space of the robot, tests them for whether they are in the free space, and uses a local
planner to attempt to connect these configurations to other nearby configurations. 
- Then starting and goal configurations are added in, and a graph search algorithm is applied to the resulting graph to determine a
path between the starting and goal configurations.
-The implementation of PRM algorithm is done in two stages. 
  1) Construction phase where a road-map is formed by approximating the
possible movement,and then it is connected to neighbors depending on the condition mentioned as parameters
such as the nearest neighbour. The configurations and connections are added to the graph when the network
becomes dense.
  2) Query phase, where the path is created for movement from initial state to goal state.
## Implementation 

## GUI Visualization
