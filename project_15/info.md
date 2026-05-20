# AGV ROS 2 Workspace

## Overview

**Type:** Robotics / ROS 2 Autonomous Ground Vehicle Simulation  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/agv_robot

AGV ROS 2 Workspace is a simulation and autonomy stack for a differential-drive Autonomous Ground Vehicle. The project models an AGV platform capable of carrying up to 600 kg and includes Gazebo simulation, 2D LiDAR SLAM, Nav2 autonomous navigation, and multiple simulation environments.

## Details

| Field | Information |
| --- | --- |
| Project name | AGV ROS 2 Workspace |
| Project type | Robotics / ROS 2 AGV Simulation |
| Robot platform | Differential-drive Autonomous Ground Vehicle |
| Main technology | ROS 2 Humble/Iron, Gazebo Harmonic, slam_toolbox, Nav2, xacro |
| Payload capacity | 600 kg |
| Build tool | colcon |
| Repository | https://github.com/pan-k15/agv_robot |

## Description

This project provides a complete simulated autonomy workflow for a warehouse-style AGV. It includes robot modeling, Gazebo worlds, ROS-Gazebo bridges, SLAM mapping, Nav2 path planning, and a one-command bringup for warehouse navigation.

The AGV can be visualized in RViz, simulated in empty, obstacle-course, or warehouse environments, mapped with `slam_toolbox`, and commanded through Nav2 goals. It is designed as a practical ROS 2 stack for learning autonomous mobile robot navigation.

## Images

Recommended screenshots to add:

- `./images/rviz-model.png` - AGV model in RViz
- `./images/warehouse-sim.png` - Warehouse Gazebo simulation
- `./images/obstacle-course.png` - Obstacle course simulation
- `./images/slam-map.png` - SLAM map output
- `./images/nav2-goal.png` - Nav2 goal execution in RViz

## Features

- ROS 2 simulation stack for a differential-drive AGV
- Gazebo Harmonic integration
- 2D LiDAR and IMU sensor modeling
- Empty world, obstacle course, and warehouse simulation environments
- `slam_toolbox` mapping and localization
- Nav2 autonomous navigation stack
- DWB local planner and NavFn global planner configuration
- Velocity smoother command flow
- RViz visualization and Nav2 goal sending
- Manual teleoperation support
- Map saving workflow with `nav2_map_server`

## Robot Specs

| Area | Detail |
| --- | --- |
| Drive type | Two-wheel differential drive |
| Chassis footprint | 927 mm x 758 mm |
| Height | About 300 mm |
| Mass | About 170 kg with battery |
| Payload capacity | 600 kg |
| Wheel radius | 80 mm |
| Wheelbase | 610 mm |
| Ground clearance | 39.5 mm |
| Sensors | 2D LiDAR and IMU |

## Packages

| Package | Purpose |
| --- | --- |
| `robot_description` | URDF/xacro robot model and display launch |
| `robot_simulation` | Gazebo worlds, robot spawn, bridges, and scan relay |
| `robot_slam` | `slam_toolbox` configuration and launch |
| `robot_navigation` | Nav2 stack configuration and bringup launch files |
| `robot_interfaces` | Planned custom messages, services, and actions |
| `robot_tasks` | Planned mission/task management |
| `robot_services` | Planned auxiliary service nodes |
| `robot_vision` | Planned camera-based perception |

## Topics And Navigation

| Topic / Component | Purpose |
| --- | --- |
| `/cmd_vel` | Final drive command sent to the robot |
| `/cmd_vel_nav` | Raw command from Nav2 controller and behaviors |
| `/scan` | LiDAR scan input for SLAM and navigation |
| `/odom` | Wheel odometry |
| `/imu` | IMU data |
| `/map` | Occupancy grid from SLAM |
| `/navigate_to_pose` | Nav2 goal action |
| `DWB` | Local planner |
| `NavFn` | Global planner |

## Links

- **GitHub:** https://github.com/pan-k15/agv_robot
- **ROS 2:** https://docs.ros.org/
- **Nav2:** https://navigation.ros.org/
- **slam_toolbox:** https://github.com/SteveMacenski/slam_toolbox
- **Gazebo:** https://gazebosim.org/

## Notes

The project includes a one-command warehouse bringup that starts the warehouse simulation, SLAM, Nav2, and RViz. The roadmap includes mission actions, task management, services, and camera/depth perception integration.
