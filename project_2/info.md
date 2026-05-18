# dofbot_ros

## Overview

**Type:** Robotics / ROS 1 Project  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/dofbot_ros

`dofbot_ros` provides ROS Noetic packages for the Yahboom DOFBOT, a 6-DOF AI Vision Robotic Arm. The project includes robot description files, hardware control, MoveIt motion-planning support, high-level task execution, and computer vision pipeline components.

## Details

| Field | Information |
| --- | --- |
| Project name | dofbot_ros |
| Project type | Robotics / ROS 1 |
| Robot platform | Yahboom DOFBOT 6-DOF robotic arm |
| Main technology | ROS Noetic, MoveIt, catkin, Python, C++ |
| Target OS | Ubuntu 20.04 |
| Repository | https://github.com/pan-k15/dofbot_ros |

## Description

This project brings the DOFBOT robotic arm into the ROS 1 ecosystem. It supports simulation, visualization, motion planning, and real robot control through a collection of ROS packages.

The repository is organized around robot configuration, MoveIt planning, hardware control, task execution, and vision. It can be used to visualize the robot in RViz, plan arm movement with MoveIt, run pick-and-place tasks, and support AI vision workflows such as QR code reading, object detection, and pose estimation.

## Images

Recommended images to add:

- `./images/rviz-preview.png` - RViz robot model preview
- `./images/dofbot-hardware.png` - DOFBOT hardware setup
- `./images/pick-and-place.png` - Pick-and-place or box-stacking demo

## Features

- ROS Noetic support for Yahboom DOFBOT
- URDF/SRDF robot description and joint configuration
- MoveIt motion planning and trajectory execution
- RViz visualization and interactive planning
- Hardware control for real robotic arm servos
- Pick-and-place and box-stacking task support
- Vision pipeline support for QR reading, object detection, and object pose estimation

## Packages

| Package | Purpose |
| --- | --- |
| `dofbot_config` | Robot description, joint configuration, and display launch files |
| `dofbot_control` | Hardware interface and servo control nodes |
| `dofbot_moveit` | MoveIt planning configuration and trajectory execution |
| `dofbot_tasks` | High-level task execution such as pick and place |
| `dofbot_vision` | Vision pipeline for QR codes, object detection, and pose estimation |

## Links

- **GitHub:** https://github.com/pan-k15/dofbot_ros
- **ROS Noetic:** https://wiki.ros.org/noetic
- **MoveIt:** https://moveit.ros.org

## Notes

The project is designed for Ubuntu 20.04 with ROS Noetic. It uses `catkin` as the build tool and includes both Python and C++ components for robot behavior, motion planning, and control.
