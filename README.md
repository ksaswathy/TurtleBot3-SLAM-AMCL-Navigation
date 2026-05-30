# ROS 2 TurtleBot3 Burger - SLAM, AMCL and Navigation

## Overview

This project demonstrates autonomous navigation using TurtleBot3 Burger in Gazebo simulation with ROS 2.

## Technologies

- ROS 2 Humble
- TurtleBot3 Burger
- Gazebo
- SLAM Toolbox
- AMCL
- Navigation2 (Nav2)
- RViz2

## Project Workflow

### 1. Launch TurtleBot3 Simulation

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```

### 2. Perform SLAM Mapping

```bash
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
```

### 3. Save Generated Map

```bash
ros2 run nav2_map_server map_saver_cli -f my_map
```

### 4. Run Localization

```bash
ros2 launch turtlebot3_navigation2 navigation2.launch.py use_sim_time:=True map:=./maps/my_map.yaml
```

### 5. Goal Based Navigation

Set navigation goals in RViz2 using the Nav2 Goal Tool.

## Results

Screenshots available in the screenshots folder.

## Author

Akhil Rajeev
