# UGV Rover PT — ROS 2 Workspace

## Overview

**Type:** Robotics / ROS 2 UGV Simulation  
**Status:** In Progress  
**GitHub:** https://github.com/pan-k15/ugv_robot

UGV Rover PT is a ROS 2 workspace for the Waveshare UGV Rover PT platform. It includes robot description, Gazebo Harmonic simulation, ROS-Gazebo bridges, sensor modeling, and online SLAM mapping with `slam_toolbox`.

## Details

| Field | Information |
| --- | --- |
| Project name | UGV Rover PT — ROS 2 Workspace |
| Project type | Robotics / ROS 2 UGV Simulation |
| Robot platform | Waveshare UGV Rover PT |
| Main technology | ROS 2 Jazzy, Gazebo Harmonic, slam_toolbox, xacro, RViz |
| Controller platform | Raspberry Pi 4B / Raspberry Pi 5 kit |
| Build tool | colcon |
| License | Apache-2.0 |
| Repository | https://github.com/pan-k15/ugv_robot |

## Description

This project models the Waveshare UGV Rover PT as a six-wheel skid-steer ground vehicle with a pan-tilt camera arm and deck-mounted sensor suite. It supports RViz visualization, Gazebo simulation, obstacle-world testing, and online mapping.

The simulated robot publishes drive, odometry, TF, joint state, LiDAR, camera, depth camera, point cloud, IMU, and clock topics. Nav2, custom services, task logic, and perception nodes are scaffolded for future expansion.

## Images

Recommended screenshots to add:

- `./images/rviz-model.png` - UGV Rover PT model in RViz
- `./images/gazebo-obstacles.png` - Obstacle world simulation
- `./images/slam-map.png` - Online SLAM map output
- `./images/pan-tilt-camera.png` - Pan-tilt camera arm view
- `./images/sensor-suite.png` - LiDAR, camera, depth, and IMU visualization

## Features

- ROS 2 workspace for Waveshare UGV Rover PT
- Six-wheel skid-steer robot model
- Pan-tilt RGB camera arm
- Depth/IR sensor and point cloud output
- Front camera simulation
- Deck-mounted LiDAR simulation
- IMU simulation
- Gazebo Harmonic empty and obstacle worlds
- ROS-Gazebo bridge for sensor and motion topics
- Online SLAM mapping with `slam_toolbox`
- RViz model visualization with joint slider GUI
- Scaffolded packages for Nav2, services, tasks, interfaces, and vision

## Robot Specs

| Area | Detail |
| --- | --- |
| Robot | Waveshare UGV Rover PT |
| Drive | Six-wheel skid-steer |
| Weight | About 3.5 kg |
| Size | 252 mm x 230 mm x 94 mm |
| Wheel radius | 41.87 mm |
| Wheel separation | About 178 mm |
| Ground clearance | 25.13 mm |
| Camera arm | Pan +/-90 degrees, tilt -30 to +60 degrees |
| Sensors | LiDAR, RGB camera, depth camera, front camera, IMU |

## Packages

| Package | Status | Purpose |
| --- | --- | --- |
| `robot_description` | Active | Xacro URDF model and RViz visualization launch |
| `robot_simulation` | Active | Gazebo Harmonic simulation, bridge, and worlds |
| `robot_slam` | Active | Online mapping with `slam_toolbox` |
| `robot_interfaces` | Scaffold | Custom messages, services, and actions |
| `robot_navigation` | Scaffold | Planned Nav2 integration |
| `robot_services` | Scaffold | Planned custom ROS 2 service nodes |
| `robot_tasks` | Scaffold | Planned high-level task logic |
| `robot_vision` | Scaffold | Planned camera and perception nodes |

## Topics

| Topic | Purpose |
| --- | --- |
| `/cmd_vel` | Drive command from ROS to Gazebo |
| `/odom` | Wheel odometry |
| `/scan` | LiDAR scan |
| `/imu/data` | IMU data |
| `/camera/image_raw` | Pan-tilt RGB camera stream |
| `/depth_camera/image_raw` | Depth camera image |
| `/depth_camera/points` | Depth point cloud |
| `/front_camera/image_raw` | Front stereo-bar camera stream |
| `/map` | Occupancy grid from SLAM |

## Links

- **GitHub:** https://github.com/pan-k15/ugv_robot
- **ROS 2 Jazzy:** https://docs.ros.org/en/jazzy/
- **Gazebo:** https://gazebosim.org/
- **slam_toolbox:** https://github.com/SteveMacenski/slam_toolbox
- **Waveshare UGV Rover PT:** https://www.waveshare.com/

## Notes

The current active packages cover robot description, simulation, and SLAM. Navigation, service nodes, high-level tasks, custom interfaces, and camera-based perception are scaffolded for future development.
