# dofbot_ros2

## Overview

**Type:** Robotics / ROS 2 Project  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/dofbot_ros2

`dofbot_ros2` provides ROS 2 packages for the Yahboom DOFBOT, a 6-DOF AI Vision Robotic Arm. The project focuses on robot configuration and MoveIt 2 motion-planning support for controlling and simulating DOFBOT under ROS 2 Humble.

## Details

| Field | Information |
| --- | --- |
| Project name | dofbot_ros2 |
| Project type | Robotics / ROS 2 |
| Robot platform | Yahboom DOFBOT 6-DOF robotic arm |
| Main technology | ROS 2 Humble, MoveIt 2, colcon, Python, C++ |
| Target OS | Ubuntu 22.04 |
| Repository | https://github.com/pan-k15/dofbot_ros2 |

## Description

This project ports DOFBOT support into the ROS 2 ecosystem. It includes robot description and MoveIt 2 configuration packages for visualizing the robotic arm, planning movements, and running simulated motion-planning demos in RViz.

The repository is useful for robotics development, ROS 2 migration work, and learning how to configure a 6-DOF arm with MoveIt 2. It provides the foundation for robot modeling, kinematics configuration, controller setup, and interactive motion planning.

## Images

Recommended images to add:

- `./images/rviz-preview.png` - RViz robot model preview
- `./images/moveit2-demo.png` - MoveIt 2 planning demo
- `./images/dofbot-workspace.png` - DOFBOT ROS 2 workspace or hardware setup

## Features

- ROS 2 Humble support for Yahboom DOFBOT
- URDF/XACRO robot model and SRDF configuration
- MoveIt 2 motion-planning integration
- RViz visualization with interactive planning
- Controller configuration for ROS 2 control
- Launch files for robot state publishing, MoveIt, and demos
- Foundation for future robotic arm task and hardware-control workflows

## Packages

| Package | Purpose |
| --- | --- |
| `dofbot_config` | Robot description, joint configuration, controller config, and launch files |
| `dofbot_moveit` | MoveIt 2 planning integration, trajectory execution, and demo launch files |

## Links

- **GitHub:** https://github.com/pan-k15/dofbot_ros2
- **ROS 2 Humble:** https://docs.ros.org/en/humble/
- **MoveIt 2:** https://moveit.picknik.ai

## Notes

The project is designed for Ubuntu 22.04 with ROS 2 Humble. It uses `colcon` as the build tool and focuses on ROS 2 robot configuration, MoveIt 2 integration, and RViz-based motion-planning demos.
