# JetCobot ROS

## Overview

**Type:** Robotics / ROS 1 Project  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/jetcobot_ros

JetCobot ROS is a ROS 1 Noetic catkin workspace for the Yahboom JetCobot, a 7-axis visual collaborative robotic arm powered by NVIDIA Jetson. The project provides robot description files, MoveIt motion-planning configuration, and control nodes for simulation and real hardware deployment.

## Details

| Field | Information |
| --- | --- |
| Project name | JetCobot ROS |
| Project type | Robotics / ROS 1 |
| Robot platform | Yahboom JetCobot 7-axis robotic arm |
| Main controller | NVIDIA Jetson Nano / Orin Nano / Orin NX |
| Main technology | ROS Noetic, MoveIt, catkin, C++, Python, RViz, Gazebo |
| Target OS | Ubuntu 20.04 |
| Repository | https://github.com/pan-k15/jetcobot_ros |

## Description

This project brings the Yahboom JetCobot robotic arm into the ROS 1 ecosystem. It includes URDF robot models, mesh assets, MoveIt configuration packages, and control code for motion planning, inverse kinematics, and joint trajectory execution.

The workspace supports both simulation and hardware-oriented workflows. Developers can visualize the robot in RViz, run MoveIt planning demos, test kinematics, and build control nodes for real arm movement. The project also documents the platform's broader capabilities, including vision integration and multiple control modes.

## Images

Recommended screenshots to add:

- `./images/rviz-preview.png` - JetCobot robot model in RViz
- `./images/moveit-planning.png` - MoveIt planning demo
- `./images/gazebo-simulation.png` - Gazebo simulation view
- `./images/hardware-setup.png` - JetCobot hardware setup

## Features

- ROS Noetic catkin workspace for Yahboom JetCobot
- URDF robot description and mesh assets for visualization
- MoveIt configuration for motion planning
- RViz visualization and interactive planning workflows
- Gazebo simulation launch support
- C++ control nodes for motion execution and kinematics testing
- Support for inverse kinematics and coordinate-based end-effector control
- Collision-aware trajectory planning with OMPL planners
- Foundation for hardware deployment on NVIDIA Jetson boards

## Packages

| Package | Purpose |
| --- | --- |
| `jetcobot_description` | URDF model, joint definitions, mesh assets, RViz and Gazebo visualization |
| `jetcobot_control` | C++ control nodes for joint commands, inverse kinematics, and motion execution |
| `jetcobot_config` | MoveIt setup with planning groups, SRDF, and kinematics configuration |
| `jetcobot_config_v2` | Updated MoveIt configuration with revised planning parameters |

## Hardware Overview

| Spec | Detail |
| --- | --- |
| Robot | Yahboom JetCobot 7-axis robotic arm |
| Controller | NVIDIA Jetson Nano 4GB / Orin Nano / Orin NX |
| Degrees of freedom | 7-axis |
| Effective arm span | 270 mm |
| Joint rotation range | -153 degrees to +153 degrees |
| Camera | 0.3MP USB camera, 110 degree FOV |

## Links

- **GitHub:** https://github.com/pan-k15/jetcobot_ros
- **Yahboom JetCobot:** https://category.yahboom.net/products/jetcobot
- **ROS Noetic:** https://wiki.ros.org/noetic
- **MoveIt:** https://moveit.ros.org/

## Notes

This is a ROS 1 Noetic workspace and is intended for Ubuntu 20.04. The repository includes two MoveIt configuration versions: `jetcobot_config` and `jetcobot_config_v2`, with the v2 package intended as the newer planning configuration.
