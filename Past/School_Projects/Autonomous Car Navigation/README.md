# Autonomous Car Navigation with Mission-Level Planning

## Overview
This project implements an autonomous navigation system for a car-like robot operating in a known indoor environment. The robot localizes itself, plans collision-free paths under non-holonomic constraints, and executes a multi-waypoint mission driven by time and resource constraints. Once initialized, the system runs autonomously without human intervention.
The robot must visit selected locations that provide different benefits and return to a final endpoint before a deadline. Constraints on visit order and repetition require careful sequencing, highlighting the interaction between planning, localization, and control.

## System Pipeline

The autonomy stack is organized as a modular pipeline:

1. **Localization:** Particle-filter-based pose estimation using a known static map  
2. **Motion Planning:** Global planning in SE(2) using a Probabilistic Roadmap (PRM) with A* search  
3. **Kinematic Constraints:** Curvature-constrained planning for Ackermann steering (non-holonomic vehicle)  
4. **Control:** Velocity-based path-following controller for continuous trajectory execution  
5. **Mission Logic:** Task-level sequencing, constraint enforcement, and mission success evaluation  

Planning is performed in a static environment with collision checking against known obstacles. The system does not use SLAM or dynamic obstacle avoidance.

## Tools 
- Python, ROS, MuSHR, Gazebo, RVIZ

## Demo
![Autonomous Navigation Demo](car.gif)

### Code available upon request.
