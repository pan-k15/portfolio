# arm6dof - Cargo Handling Robot Arm

## Overview

**Type:** Robotics / ROS 2 Manipulator Simulation  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/cargo_handling_robot_arm

Cargo Handling Robot Arm is a ROS 2 Jazzy and Gazebo Harmonic simulation of a 6-DOF robotic arm with a 2-finger parallel gripper. The project includes robot description, Gazebo simulation, ROS 2 control configuration, custom pick/place services, and C++ service servers for simple cargo-handling workflows.

## Details

| Field | Information |
| --- | --- |
| Project name | arm6dof - Cargo Handling Robot Arm |
| Project type | Robotics / ROS 2 Manipulator Simulation |
| Robot platform | 6-DOF arm with 2-finger parallel gripper |
| Main technology | ROS 2 Jazzy, Gazebo Harmonic, ros2_control, C++, xacro |
| Build tool | colcon |
| Repository | https://github.com/pan-k15/cargo_handling_robot_arm |

## Description

This project models a 6-DOF robotic arm using simple primitive geometry, so it can run without external mesh assets. The arm includes six revolute joints and a parallel gripper with prismatic finger motion.

The simulation supports joint trajectory control, gripper commands, and pick/place service calls. The pick and place logic uses a simple geometric 2R inverse kinematics approach for moving to target poses, closing or opening the gripper, and lifting or retracting from the object.

## Images

Recommended screenshots to add:

- `./images/rviz-model.png` - Arm model in RViz
- `./images/gazebo-simulation.png` - Gazebo simulation view
- `./images/pick-service.png` - Pick operation demo
- `./images/place-service.png` - Place operation demo
- `./images/gripper-closeup.png` - Parallel gripper close-up

## Features

- 6-DOF robot arm model built with primitive shapes
- 2-finger parallel gripper with mimic-style motion
- ROS 2 Jazzy and Gazebo Harmonic simulation
- `ros2_control` controller setup
- RViz display launch with joint slider GUI
- Arm trajectory controller for six joints
- Gripper forward command controller
- Custom `Pick.srv` and `Place.srv` interfaces
- C++ pick and place service servers
- Geometric inverse kinematics for simple target poses

## Packages

| Package | Purpose |
| --- | --- |
| `robot_description` | URDF/xacro model, RViz config, and standalone visualization launch |
| `robot_simulation` | Gazebo world, controller config, and full simulation launch |
| `robot_interfaces` | Custom service definitions for pick and place |
| `robot_services` | C++ pick and place service servers |
| `moveit_config` | MoveIt 2 configuration for the arm |
| `robot_vision` | Planned object detection and pose estimation package |

## Controllers And Services

| Name | Purpose |
| --- | --- |
| `joint_state_broadcaster` | Publishes all joint states |
| `arm_controller` | Controls `joint1` through `joint6` with position trajectories |
| `gripper_controller` | Controls the gripper finger command |
| `/pick` | Moves to pre-grasp, grasps, and lifts |
| `/place` | Moves to pre-place, releases, and retracts |

## Links

- **GitHub:** https://github.com/pan-k15/cargo_handling_robot_arm
- **ROS 2 Jazzy:** https://docs.ros.org/en/jazzy/
- **Gazebo:** https://gazebosim.org/

## Notes

The arm has a TCP reach of about 0 to 0.83 m from joint 2. The project is suitable for learning ROS 2 manipulator simulation, controller setup, custom services, and simple pick-and-place behavior.
