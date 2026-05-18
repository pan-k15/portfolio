# AgriBot Rover

## Overview

**Type:** Robotics / ROS 2 Rover Simulation  
**Status:** In Progress  
**GitHub:** https://github.com/pan-k15/agribot

AgriBot Rover is an autonomous all-terrain robot concept designed to transport agricultural waste from hillside farms to roadside collection points. It was developed for the AgriSpark Hackathon 2025, "Hack the Hills", and focuses on reducing labor, time, and risk for farmers working in mountainous areas.

## Details

| Field | Information |
| --- | --- |
| Project name | AgriBot Rover |
| Project type | Robotics / ROS 2 Rover Simulation |
| Robot platform | Skid-steer agricultural rover |
| Main technology | ROS 2 Jazzy, Gazebo Harmonic, xacro, RViz |
| Payload target | 10-15 kg |
| Terrain | 40 m x 40 m hillside with about 8 m elevation change |
| Repository | https://github.com/pan-k15/agribot |

## Description

This project simulates an agricultural rover for moving post-harvest corn waste across uneven hillside terrain. The rover is designed with a wider V2 chassis, four driven wheels, a cargo bed, side walls, a front bumper, LiDAR, and a forward-facing camera.

The simulation includes a hillside Gazebo world generated from a heightmap, ROS-Gazebo bridges for core topics, and launch files for full simulation or quick empty-world testing. The roadmap includes IMU/GPS localization, Nav2 path planning, SLAM, cargo sensing, and a web monitoring dashboard.

## Images

Recommended screenshots to add:

- `./images/rviz-model.png` - AgriBot model in RViz
- `./images/hillside-world.png` - Hillside Gazebo world
- `./images/grass-terrain.png` - Terrain and grass environment
- `./images/teleop-demo.png` - Teleoperation demo
- `./images/cargo-bed.png` - Cargo bed and rover body close-up

## Features

- ROS 2 Jazzy rover simulation
- Skid-steer 4-wheel differential drive
- V2 rover body with cargo bed, cargo walls, and bumper
- 2D LiDAR sensor simulation
- Monocular camera simulation
- Gazebo Harmonic hillside terrain world
- ROS-Gazebo bridge for drive, odometry, LiDAR, camera, TF, and clock topics
- RViz model viewer
- Teleoperation support
- Heightmap terrain generation script
- Roadmap for IMU, GPS, Nav2, SLAM, and web dashboard

## Robot Specs

| Area | Detail |
| --- | --- |
| Drive type | Skid-steer 4-wheel differential |
| Payload capacity | 10-15 kg |
| Chassis size | 0.70 m x 0.55 m x 0.10 m |
| Wheel radius | 0.10 m |
| Track width | 0.66 m |
| Wheelbase | 0.46 m |
| Sensors | 2D LiDAR and monocular camera |
| Main terrain | 40 m x 40 m hillside |

## Packages

| Package | Purpose |
| --- | --- |
| `rover_description` | Robot model, URDF/xacro files, meshes, RViz config, and display launch |
| `world_simulation` | Gazebo worlds, hillside terrain model, bridge config, launch files, and heightmap script |

## Links

- **GitHub:** https://github.com/pan-k15/agribot
- **ROS 2 Jazzy:** https://docs.ros.org/en/jazzy/
- **Gazebo:** https://gazebosim.org/

## Notes

The current implementation includes the V2 robot model, hillside world, ROS-Gazebo bridge, and teleoperation-ready simulation. Navigation, SLAM, localization, cargo sensing, and dashboard features are planned next steps.
