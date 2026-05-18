# UR3 Gripper - UR Gazebo + MoveIt Simulation

## Overview

**Type:** Robotics / ROS 2 Manipulator Simulation  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/ur3_gripper

UR3 Gripper is a ROS 2 Jazzy workspace for simulating a Universal Robots arm with a Robotiq 2F-85 gripper in Gazebo and MoveIt 2. The project includes UR robot description packages, gripper visualization, MoveIt configuration, Gazebo worlds, ROS-Gazebo bridges, and pick/place control components.

## Details

| Field | Information |
| --- | --- |
| Project name | UR3 Gripper - UR Gazebo + MoveIt Simulation |
| Project type | Robotics / ROS 2 Manipulator Simulation |
| Robot platform | Universal Robots arm with Robotiq 2F-85 gripper |
| Main technology | ROS 2 Jazzy, Gazebo, MoveIt 2, ros2_control, C++, xacro |
| Build tool | colcon |
| Repository | https://github.com/pan-k15/ur3_gripper |

## Description

This project provides a complete simulated manipulation stack for a Universal Robots arm and Robotiq 2F-85 gripper. The simulation launch starts Gazebo, robot state publishing, ROS-Gazebo bridge nodes, robot spawning, controller spawners, MoveIt `move_group`, and RViz when enabled.

The workspace includes multiple Gazebo worlds for testing pick-and-place behavior, residential and warehouse scenes, blocks, tables, and object models. It also includes custom robot interfaces and pick/place service or action code for higher-level manipulation workflows.

## Images

Recommended screenshots to add:

- `./images/gazebo-simulation.png` - UR arm and gripper in Gazebo
- `./images/moveit-planning.png` - MoveIt motion planning in RViz
- `./images/robotiq-gripper.png` - Robotiq 2F-85 gripper close-up
- `./images/pick-place-demo.png` - Pick-and-place world demo
- `./images/point-cloud-view.png` - Point cloud visualization

## Features

- Universal Robots arm simulation in Gazebo
- Robotiq 2F-85 gripper model and visualization package
- MoveIt 2 configuration for planning and execution
- ROS-Gazebo bridge configuration
- Controller spawners for arm and gripper controllers
- RViz MoveIt planning interface
- Gazebo worlds for pick-and-place and object interaction demos
- Custom pick/place service and action interfaces
- C++ robot control and service server components
- Point cloud viewer launch support

## Packages

| Package | Purpose |
| --- | --- |
| `ur_description` | UR robot description, xacro macros, meshes, and launch files |
| `robotiq_2f_85_gripper_visualization` | Robotiq gripper meshes, URDF/xacro model, and visualization config |
| `moveit_config` | MoveIt 2 planning configuration for the arm and gripper |
| `ur_gazebo` | Gazebo worlds, ROS-Gazebo bridge config, and simulation launch files |
| `robot_interfaces` | Custom pick/place service and action definitions |
| `robot_services` | Pick/place service and action server code |
| `robot_control` | Pick-and-place control launch and C++ control code |

## Simulation Workflow

| Step | Description |
| --- | --- |
| 1 | Launch Gazebo with the selected world |
| 2 | Publish robot state from `/robot_description` |
| 3 | Spawn the robot into Gazebo |
| 4 | Start ROS-Gazebo bridge nodes |
| 5 | Spawn joint, arm, and gripper controllers |
| 6 | Start MoveIt `move_group` |
| 7 | Open RViz for planning and visualization |

## Links

- **GitHub:** https://github.com/pan-k15/ur3_gripper
- **ROS 2 Jazzy:** https://docs.ros.org/en/jazzy/
- **MoveIt 2:** https://moveit.picknik.ai/
- **Gazebo:** https://gazebosim.org/
- **Universal Robots ROS 2 Description:** https://github.com/UniversalRobots/Universal_Robots_ROS2_Description

## Notes

The repository contains many Gazebo scene assets and object models for manipulation testing, including pick-and-place demo worlds, residential environments, warehouse items, blocks, tables, and point cloud visualization support.
