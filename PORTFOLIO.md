# Portfolio
## Pan Kraiwattanapong

---

## About Me

I am a self-taught developer and robotics engineer building open-source projects across robotics, AI, and software. My work spans ROS 1 and ROS 2 simulation stacks, computer vision pipelines, machine learning web apps, and full desktop applications — all built independently, driven by curiosity and the challenge of making things work from scratch.

My primary focus is on robotics: designing and simulating robot systems end-to-end, from URDF modeling and Gazebo environments to autonomous navigation with SLAM and Nav2, manipulation with MoveIt, and task-level control. Alongside that, I build practical AI and computer vision tools — deploying real trained models into usable interfaces rather than stopping at notebooks.

Everything I publish is open source. I share complete, working codebases so others learning robotics or machine learning can use them as references, starting points, or learning material.

---

## Skills at a Glance

**Robotics**
ROS 1 Noetic, ROS 2 Humble / Iron / Jazzy, Gazebo Classic, Gazebo Harmonic, MoveIt, MoveIt 2, Nav2, slam_toolbox, ros2_control, xacro, URDF, SRDF, colcon, catkin

**AI and Machine Learning**
PyTorch, YOLO, EasyOCR, HuggingFace Transformers, spaCy, NLTK, OpenCV, deep learning image classification, object detection, OCR pipelines, NLP

**Programming**
Python, C++, SQL

**Web and Desktop**
Flask, Streamlit, Vue 3, Vite, TailwindCSS, Vue Router, Python Tkinter, customtkinter

**Data and Backend**
SQLite, Firebase Firestore, Pandas, openpyxl, Pillow

---

## Projects

### Robotics and Simulation

---

#### Palm Harvester — ROS 2 Mobile Manipulator
**Type:** ROS 2 Simulation | **Status:** In Progress

A tracked mobile manipulator designed for autonomous palm fruit harvesting. The robot combines a heavy-duty tracked base (180 kg chassis) with a 5-DOF arm and a high-speed sickle blade end-effector capable of spinning up to approximately 314 rad/s.

The system runs on ROS 2 Jazzy with Gazebo Harmonic and includes full sensor integration: Ouster LiDAR, Intel RealSense D455, RGB camera, IMU, and GPS. SLAM mapping with slam_toolbox, ROS 2 controllers for the tracked base, arm trajectory, and blade velocity are all functional. Planned work includes Nav2 navigation, custom task sequencing, a vision pipeline, and high-level harvesting services.

**Technologies:** ROS 2 Jazzy, Gazebo Harmonic, gz_ros2_control, slam_toolbox, xacro, colcon

**Key technical points:**
- Tracked differential-drive base simulation
- 5-DOF arm with prismatic boom extension and sickle blade end-effector
- Full sensor topic suite: LiDAR, IMU, RGB camera, depth camera, point cloud
- Farm world, obstacle world, and empty world simulation environments
- SLAM support with slam_toolbox
- Multi-package workspace: description, simulation, SLAM, and scaffolded navigation and vision packages

---

#### AGV ROS 2 Workspace
**Type:** ROS 2 AGV Simulation | **Status:** Completed

A complete autonomy stack for a warehouse-class Autonomous Ground Vehicle rated for 600 kg payload. The project covers the full navigation workflow: robot modeling, Gazebo simulation, SLAM mapping, and Nav2 autonomous navigation with a single-command warehouse bringup.

**Technologies:** ROS 2 Humble / Iron, Gazebo Harmonic, slam_toolbox, Nav2, xacro, colcon

**Robot specs:** 927 mm x 758 mm footprint, ~170 kg, 600 kg payload, differential drive, 2D LiDAR and IMU

**Key technical points:**
- Gazebo Harmonic simulation with empty, obstacle-course, and warehouse environments
- SLAM mapping and localization with slam_toolbox
- Nav2 stack: DWB local planner, NavFn global planner, velocity smoother
- RViz visualization with Nav2 goal sending
- Map saving workflow with nav2_map_server
- Multi-package workspace with scaffolded mission and perception packages

---

#### UR3 Gripper — UR Gazebo + MoveIt Simulation
**Type:** ROS 2 Manipulator Simulation | **Status:** Completed

A complete simulated manipulation stack for a Universal Robots arm with a Robotiq 2F-85 gripper. The simulation launch orchestrates Gazebo, robot state publisher, ROS-Gazebo bridge nodes, controller spawners, MoveIt move_group, and RViz in a single workflow.

**Technologies:** ROS 2 Jazzy, Gazebo, MoveIt 2, ros2_control, C++, xacro

**Key technical points:**
- UR robot description with full xacro macros and mesh assets
- Robotiq 2F-85 gripper model and visualization package
- MoveIt 2 motion planning configuration and RViz planning interface
- Multiple Gazebo pick-and-place worlds with object models and warehouse scenes
- Custom pick/place service and action interfaces
- C++ service servers and robot control launch components

---

#### Cargo Handling Robot Arm — arm6dof
**Type:** ROS 2 Manipulator Simulation | **Status:** Completed

A 6-DOF robotic arm with a 2-finger parallel gripper built from primitive geometry, designed to run without external mesh assets. Implements custom pick and place services backed by geometric inverse kinematics.

**Technologies:** ROS 2 Jazzy, Gazebo Harmonic, ros2_control, C++, xacro

**Key technical points:**
- 6-DOF arm with prismatic parallel gripper
- Custom Pick.srv and Place.srv interfaces with C++ service servers
- Geometric 2R inverse kinematics for target pose calculation
- Arm trajectory controller and gripper forward command controller
- MoveIt 2 configuration included
- TCP reach of approximately 0 to 0.83 m from joint 2

---

#### UGV Rover PT — ROS 2 Workspace
**Type:** ROS 2 UGV Simulation | **Status:** In Progress

A ROS 2 simulation workspace for the Waveshare UGV Rover PT, a six-wheel skid-steer ground vehicle with a pan-tilt camera arm. Publishes full sensor topics and supports online SLAM mapping.

**Technologies:** ROS 2 Jazzy, Gazebo Harmonic, slam_toolbox, xacro

**Robot specs:** 252 mm x 230 mm x 94 mm, ~3.5 kg, six-wheel skid-steer, pan-tilt camera (+/-90 pan, -30 to +60 tilt)

**Key technical points:**
- LiDAR, RGB camera, depth camera, front camera, IMU simulation
- ROS-Gazebo bridge for all sensor and motion topics
- Online SLAM mapping with slam_toolbox
- Obstacle world and empty world environments
- Scaffolded packages for Nav2, services, tasks, and vision

---

#### AgriBot Rover
**Type:** ROS 2 Rover Simulation | **Status:** In Progress

Built for the AgriSpark Hackathon 2025 "Hack the Hills" challenge. AgriBot is an autonomous all-terrain agricultural rover designed to carry 10–15 kg of post-harvest crop waste across 40 m x 40 m hillside terrain with approximately 8 m of elevation change.

**Technologies:** ROS 2 Jazzy, Gazebo Harmonic, xacro, RViz

**Key technical points:**
- Skid-steer 4-wheel rover with cargo bed, side walls, and front bumper
- Gazebo hillside world generated from a heightmap
- 2D LiDAR and monocular camera simulation
- ROS-Gazebo bridge for drive, odometry, sensors, TF, and clock
- Heightmap terrain generation script
- Roadmap includes IMU/GPS localization, Nav2, SLAM, and a web monitoring dashboard

---

#### JetCobot ROS
**Type:** ROS 1 Robotics | **Status:** Completed

ROS 1 Noetic catkin workspace for the Yahboom JetCobot, a 7-axis visual collaborative arm running on an NVIDIA Jetson board. Includes URDF model, mesh assets, MoveIt configuration, and C++ control nodes for inverse kinematics and trajectory execution.

**Technologies:** ROS Noetic, MoveIt, catkin, C++, Python, RViz, Gazebo

**Robot specs:** 7-axis, 270 mm effective arm span, joint range -153 to +153 degrees, Jetson Nano / Orin platform

**Key technical points:**
- Full URDF model with mesh assets for RViz and Gazebo
- Two MoveIt configuration packages with OMPL planners and collision-aware planning
- C++ control nodes for joint commands and end-effector coordinate control
- Hardware deployment target: NVIDIA Jetson Nano / Orin Nano / Orin NX

---

#### dofbot_ros2
**Type:** ROS 2 Robotics | **Status:** Completed

ROS 2 Humble packages for the Yahboom DOFBOT 6-DOF AI Vision Robotic Arm. Provides robot description and MoveIt 2 configuration for visualization, motion planning, and simulated trajectory execution.

**Technologies:** ROS 2 Humble, MoveIt 2, colcon, Python, C++

---

#### dofbot_ros
**Type:** ROS 1 Robotics | **Status:** Completed

ROS 1 Noetic packages for the Yahboom DOFBOT 6-DOF arm covering simulation, hardware control, MoveIt planning, task execution, and a vision pipeline for QR codes, object detection, and pose estimation.

**Technologies:** ROS Noetic, MoveIt, catkin, Python, C++

---

### AI, Machine Learning, and Computer Vision

---

#### Med Slip OCR Project
**Type:** OCR / Computer Vision Web App | **Status:** Completed

Built during the Super AI Engineer Internship at Botnoi. The project automates data entry from medical slip images by combining a custom YOLO detection model with EasyOCR. The pipeline detects text regions, crops them, runs OCR, and exports structured readings — date, time, systolic pressure, diastolic pressure, and pulse — to CSV.

**Technologies:** Python, Streamlit, PyTorch, YOLO (custom trained model), EasyOCR, OpenCV, Pandas

**Workflow:** Upload images → YOLO region detection → crop → EasyOCR → structured CSV export

---

#### NLP Web App — Streamlit
**Type:** NLP / Machine Learning Web App | **Status:** Completed

An all-in-one NLP playground that combines classical NLP tools with modern Transformer models in a single Streamlit interface. Covers question answering, text summarization, sentiment analysis, named entity recognition, part-of-speech tagging, word and sentence segmentation, and an interactive tokenizer demo.

**Technologies:** Python, Streamlit, HuggingFace Transformers, PyTorch, spaCy, NLTK

**Models used:**
- Question answering: deepset/roberta-base-squad2
- Summarization: facebook/bart-large-cnn
- Sentiment analysis: siebert/sentiment-roberta-large-english
- Tokenizer demo: distilbert-base-uncased

---

#### Object Detection Web App
**Type:** Computer Vision Web App | **Status:** Completed

A browser-based YOLOv5 object detection interface built with Streamlit. Users upload multiple images, set a confidence threshold, and receive annotated output images alongside a structured detection table showing class names, bounding boxes, and confidence scores.

**Technologies:** Python, Streamlit, YOLOv5, Ultralytics, PyTorch, OpenCV, Pillow, Pandas

---

#### Image Classification Webapp
**Type:** AI / Machine Learning Web App | **Status:** Completed

A Flask web application that deploys a CIFAR-10 deep learning image classifier. Users upload an image through the browser; the backend processes it with the trained model and returns the predicted class as text.

**Technologies:** Python, Flask, HTML, CSS, Bootstrap, deep learning (CIFAR-10 classifier)

---

### Desktop and Web Applications

---

#### GymFlow Pro
**Type:** Desktop Fitness Management Application | **Status:** Completed

A modern customtkinter desktop application for BK Sports Complex. Manages gym members, QR check-in, check-in records, training packages with FIFO session deduction, trainer management, and IDP CUBO3 CR-80 PVC membership card printing. Backed by Firebase Firestore with a local mock-data fallback for development.

**Technologies:** Python, customtkinter, Firebase Firestore, Pillow, qrcode, openpyxl

**Key features:** Member CRUD with photo upload, auto member IDs, QR scanner integration, date-range check-in filters, CSV and Excel export, card print preview

---

#### BK Sports Complex — Gym Member Management System
**Type:** Desktop Management Application | **Status:** Completed

A fully offline desktop management system built with Python and Tkinter. Stores all data locally in SQLite with no internet connection required. Supports RFID card enrollment, QR scanning, manual check-in, training session tracking, membership card generation, and IDP CUBO3 card printer integration.

**Technologies:** Python, Tkinter, SQLite, Pillow, qrcode, openpyxl

---

#### Dogcare Management App
**Type:** Web Management Application | **Status:** In Progress

An internal management system for a multi-service dogcare facility covering dog run, cafe, wash and dry, grooming, and a snack shop. Built with Vue 3 and structured across 15 pages for booking, scheduling, member management, service operations, inventory, reports, and staff roles.

**Technologies:** Vue 3, Vite, Vue Router, TailwindCSS, FullCalendar

---

## Summary

| Area | Count | Notable |
| --- | --- | --- |
| Robotics / ROS projects | 9 | ROS 1 and ROS 2, manipulators, rovers, AGV, mobile manipulator |
| AI / ML / CV projects | 4 | YOLO, Transformers, OCR, image classification |
| Desktop and web apps | 3 | Gym management, dogcare booking, card printing |
| **Total** | **16** | |

**ROS versions covered:** ROS Noetic, ROS 2 Humble, ROS 2 Iron, ROS 2 Jazzy

**Simulation environments:** Gazebo Classic, Gazebo Harmonic — empty worlds, warehouse, farm/hillside terrain, pick-and-place scenes

**Navigation and manipulation:** Nav2, MoveIt, MoveIt 2, slam_toolbox, OMPL planners, ros2_control

---

## Why I'm Seeking Support

All of these projects are built on personal time, personal hardware, and personal investment. Open-source robotics work has real costs:

- **Hardware:** Real robot arms, embedded boards (NVIDIA Jetson), sensors (LiDAR, depth cameras), and supporting equipment cost significant money. Most of my current simulation work exists because I cannot yet afford the hardware to test it on.
- **Time:** Every project represents dozens to hundreds of hours of research, implementation, debugging, and documentation. None of this is supported by an employer or institution.
- **Continuity:** Financial support means I can keep these repositories active, push them further, and take on more ambitious hardware-in-the-loop projects.

**What your support goes toward:**
- Purchasing hardware to move simulation projects to real robot deployment
- Expanding existing projects — particularly the Palm Harvester and AGV — to full autonomy with real hardware
- Building new open-source robotics and AI projects and sharing them publicly
- Maintaining and improving documentation so others can learn from the work

If any of these projects have been useful to you — as a reference, a starting point, or just something interesting to read through — a small contribution helps me keep going and build more.

---

*GitHub: pan-k15*
*All projects are publicly available on GitHub under the pan-k15 profile*
