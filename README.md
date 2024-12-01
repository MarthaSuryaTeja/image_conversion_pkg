# Image Conversion Package for ROS 2

This repository contains the `image_conversion_pkg`, a ROS 2 package designed to demonstrate image processing using OpenCV and ROS 2's `image_transport`. The package subscribes to an image topic, processes the image (e.g., converts it to grayscale), and displays it using OpenCV.

## Table of Contents

1. [Prerequisites](#prerequisites)  
2. [Repository Structure](#repository-structure)  
3. [Step-by-Step Setup](#step-by-step-setup)  
   - [Clone the Repository](#1-clone-the-repository)  
   - [Create the Workspace](#2-create-the-workspace)  
   - [Set Up the Package](#3-set-up-the-package)  
   - [Create the Source Code](#4-create-the-source-code)  
   - [Build the Package](#5-build-the-package)  
4. [Run the Node](#run-the-node)  
5. [Troubleshooting](#troubleshooting)  

## Prerequisites

Before setting up the package, ensure you have the following:

- **ROS 2 Humble Hawksbill** installed. ([Installation Guide](https://docs.ros.org/en/humble/Installation.html))
- **Installation of usb_cam package** 
    ```bash
    sudo apt-get install ros-humble-usb-cam
- OpenCV installed (usually included with `cv_bridge`).  
- `colcon` build tool installed.  
- `image_transport` and `cv_bridge` ROS 2 dependencies.

## Repository Structure

Once cloned and set up, your workspace should look like this:

```plaintext
ros2_ws/
├── src/
│   └── image_conversion_pkg/
│       ├── CMakeLists.txt
│       ├── package.xml
│       └── src/
│           └── image_converter_node.cpp
        └── launch
            └── image_conversion_launch.py
├── build/
├── install/
└── log/
