# Palm Harvester — ROS 2 Mobile Manipulator

## Overview

**Type:** Robotics / ROS 2 Simulation Project  
**Status:** In Progress  
**GitHub:** https://github.com/pan-k15/palm-harvesting-robot

Palm Harvester is a ROS 2 mobile manipulator project designed for autonomous palm fruit harvesting. The robot uses a tracked skid-steer base, a 5-DOF harvesting arm, a sickle blade end-effector, and a full sensor suite for simulation, mapping, navigation, and future perception workflows.

## Details

| Field | Information |
| --- | --- |
| Project name | Palm Harvester — ROS 2 Mobile Manipulator |
| Project type | Robotics / ROS 2 Simulation |
| Robot platform | Tracked mobile manipulator for palm fruit harvesting |
| Main technology | ROS 2 Jazzy, Gazebo Harmonic, gz_ros2_control, slam_toolbox, xacro |
| Build tool | colcon |
| License | Apache-2.0 |
| Repository | https://github.com/pan-k15/palm-harvesting-robot |

## Description

This project models and simulates a tracked harvesting robot for palm plantation environments. The robot combines a heavy mobile base with a 5-DOF arm and a high-speed sickle blade end-effector for reaching and cutting palm fruit.

The repository includes robot description files, Gazebo simulation launches, farm and obstacle worlds, controller configuration, and SLAM support. Navigation, vision, high-level services, custom interfaces, and task sequencing packages are included as planned areas for future development.

## Images

Recommended screenshots to add:

- `./images/rviz-model.png` - Robot model preview in RViz
- `./images/gazebo-farm-world.png` - Farm world simulation in Gazebo
- `./images/slam-map.png` - SLAM mapping output
- `./images/arm-control.png` - 5-DOF arm control demo
- `./images/blade-end-effector.png` - Sickle blade end-effector view

## Features

- ROS 2 Jazzy workspace for a mobile harvesting robot
- Tracked differential-drive base simulation
- 5-DOF robotic arm model with prismatic boom extension
- Sickle blade end-effector with velocity controller
- Gazebo Harmonic simulation with `gz_ros2_control`
- RViz robot visualization launch
- Farm world, obstacle world, and empty world simulation files
- SLAM support with `slam_toolbox`
- ROS 2 controllers for joint states, diff drive, arm trajectory, and blade velocity
- Sensor topics for LiDAR, IMU, RGB camera, depth camera, and point cloud
- Planned packages for Nav2, robot services, task sequencing, and perception

## Robot Specs

| Area | Detail |
| --- | --- |
| Base | 2.0 m x 1.0 m x 0.4 m chassis, 180 kg |
| Drive | Tracked differential drive |
| Track separation | 1.22 m |
| Track radius | 0.25 m |
| Max speed | 1.5 m/s forward, 1.0 rad/s yaw |
| Arm | 5-DOF arm with pan, boom pitch, boom extension, wrist pitch, and wrist roll |
| End-effector | Continuous sickle blade, up to about 314 rad/s |
| Sensors | Ouster LiDAR, RealSense D455, RGB camera, IMU, GPS |

## Packages

| Package | Purpose |
| --- | --- |
| `robot_description` | URDF/xacro model and RViz display launch |
| `robot_simulation` | Gazebo launch files, SDF worlds, controller config, and scan relay |
| `robot_slam` | `slam_toolbox` async mapping and localization |
| `robot_navigation` | Nav2 package planned for navigation |
| `robot_interfaces` | Custom messages and services planned |
| `robot_services` | High-level robot services planned |
| `robot_tasks` | Task sequencing planned |
| `robot_vision` | Perception pipeline planned |

## Controllers And Topics

| Controller / Topic | Purpose |
| --- | --- |
| `joint_state_broadcaster` | Publishes robot joint states |
| `diff_drive_controller` | Converts `/cmd_vel` into tracked base motion and publishes odometry |
| `arm_trajectory_controller` | Controls 5-DOF arm position trajectories |
| `blade_velocity_controller` | Controls sickle blade spin velocity |
| `/scan` | LiDAR scan output |
| `/imu/data` | IMU output |
| `/depth_camera/points` | Depth camera point cloud |
| `/camera/image_raw` | RGB camera image stream |

## Links

- **GitHub:** https://github.com/pan-k15/palm-harvesting-robot
- **ROS 2 Jazzy:** https://docs.ros.org/en/jazzy/
- **Gazebo:** https://gazebosim.org/
- **slam_toolbox:** https://github.com/SteveMacenski/slam_toolbox

## Notes

The project targets ROS 2 Jazzy with Gazebo Harmonic. The simulation can launch an empty world, a farm world with palm plantation rows, or a generic obstacle course. Several packages are present as planned development areas for navigation, custom interfaces, high-level services, task execution, and vision.
