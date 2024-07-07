# Gazebo world
The purpose of this repository is to create robotic simulated environment using [Gazebo](https://gazebosim.org/home), interact with it through plugins & design models with Gazebo tools like model and building editor.

## Description
Inside the Gazebo world one can identify:

* An Office environment: A building model designed on the Building Editor tool of Gazebo. The structure contains features/colors/texture and allows for enough space for a robot movement.
* Robots: Two instances of a model designed on the Model Editor tool of Gazebo. Model links are connected with joints
* Tables: A model imported from the Gazebo online library.
* Terminal: A welcome message generated from a world plugin and printed to the terminal, as soon as Gazebo world file is launched.

## Getting Started

### Directory structure
    .GazeboWorld                       # Build Gazebo World Project 
    ├── model                          # Model files 
    │   ├── Building
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── HumanoidRobot
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script      
    │   ├── welcome_message.cpp
    ├── world                          # Gazebo main World containing models 
    │   ├── UdacityOffice.world
    ├── CMakeLists.txt                 # Link libraries 
    └──                           

### Dependencies

* Operating System — Ubuntu Bionic 18.04 LTS or 20.04 LTS (Focal Fossa), and WSL on Windows
* Software packages — CMake 2.8 or later, ROS Noetic, Gazebo 11
    * [Gazebo Classic 11.0](https://classic.gazebosim.org/) will reach its end of life by Feb 2025.
    * [ROS Noetic](https://wiki.ros.org/noetic) is supported for 20.04 and will reach its end of life in May 2025.

### Installing

* [Install ROS Noetic using Ubuntu/WSL](https://wiki.ros.org/noetic/Installation/Ubuntu)
* [Install Gazebo using Ubuntu packages](https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
* [Install ROS Noetic using Robostack for Mac](https://robostack.github.io/GettingStarted.html)
* [Install Gazebo on Mac](https://classic.gazebosim.org/tutorials?tut=install_on_mac&cat=install)
* To verify installation, run
```
gazebo
```

### How to run

* How to run the program

    * Update and upgrade the Workspace
    ```
    sudo apt-get update && sudo apt-get upgrade -y
    ```
    * Clone the lab folder in /home/workspace/
    ```
    cd /home/workspace/
    git clone https://github.com/udacity/RoboND-myrobot myrobot
    ```
    * Compile code
    ```
    mkdir build
    cd build/
    cmake ../
    make # You might get errors if your system is not up to date!
    ```
    * Add the library path to the Gazebo plugin path
    ```
    export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/myrobot/build
    ```
    * Run Gazebo world
    ```
    cd /home/workspace/myrobot/world/
    gazebo myworld
    ```

## Visualize output

A ```Hello World!``` message is printed in the terminal. This message interacts with the Gazebo World that includes the two-wheeled robot.

## Reference repository

[RoboND-myrobot](https://github.com/udacity/RoboND-myrobot)
