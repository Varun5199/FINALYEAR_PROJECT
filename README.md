# FINALYEAR_PROJECT
Code for execution : Python
# Intelligent Robot Navigation with Object Detection

## Overview

This project simulates an intelligent robot navigating inside a bounded environment. The robot detects different types of objects and reacts accordingly using simple decision-making logic.

The robot can identify:

* Living objects (based on temperature)
* Non-living objects (box and sphere)
* Walls (boundary detection)



## Features

* Autonomous navigation in a closed environment
* Object detection using distance and temperature
* Different movement behaviors for different object types
* Anti-stuck mechanism using repeat detection logic
* Real-time simulation using a physics engine


## Logic Used

### 1. Detection System

The robot continuously checks:

* Distance to nearby objects
* Nearest object
* Temperature values

| Object Type | Condition      | Temperature |
| ----------- | -------------- | ----------- |
| Living      | Distance < 1.5 | 37°C        |
| Non-living  | Distance < 1.0 | 25°C        |
| Wall        | Near boundary  | N/A         |



### 2. Movement Behavior

#### Living Object

* Slows down
* Performs a smooth turn
* Continues moving forward

#### Non-Living Object

* Stops
* Moves backward
* Performs a sharp turn
* Continues forward

#### Wall

* Stops
* Moves backward
* Performs a sharp escape turn


### 3. Anti-Stuck Logic

* If the robot repeatedly detects obstacles:

  * Performs a U-turn
  * Resets the repeat counter



## Technologies Used

* Python
* Browserbotics Simulation API
* Basic physics simulation
* Mathematical distance calculation



## Project Structure

* `main.py` : Contains the complete simulation logic
* Uses `roomba.urdf` as the robot model


## How to Run

1. Install required dependencies
2. Run the script:


python main.py


## Output

* Robot moves inside a 9x9 bounded world
* Detects objects in real time
* Prints detection logs such as:

  * Living detected
  * Non-living detected
  * Wall detected



## Future Improvements

* Add camera-based detection using machine learning
* Implement advanced path planning algorithms
* Extend to multi-robot systems
* Integrate with real-world hardware



## Author

Sneha Priyya G,Varun M,Bagavan S E



It serves as a foundation for robotics and intelligent navigation systems.
