

https://github.com/user-attachments/assets/3879271f-bce6-42b3-b608-394f5121cdfe











# 🤖 My Robot Description — ROS 2

A ROS 2 robot description package for modeling and visualizing a robotic arm using **URDF/Xacro** and **RViz**.

## 📌 Project Overview

This project contains the robot's:

* 🤖 Links and joints
* 📐 Robot geometry
* 🔧 Xacro-based URDF description
* 🎨 Visual materials
* 🖥️ RViz visualization configuration
* 🚀 ROS 2 launch file

The robot model is built using Xacro and can be visualized in RViz.

## 🛠️ Technologies Used

* **ROS 2 Humble**
* **Ubuntu 22.04**
* **URDF**
* **Xacro**
* **RViz2**
* **CMake**
* **Git / GitHub**
* **WSL2**

## 📂 Package Structure

```text
my_robot_de/
├── launch/
│   └── display.launch.xml
├── rviz/
│   └── urdf_config.rviz
├── urdf/
│   ├── arm.xacro
│   ├── common_properties.xacro
│   └── my_robot.urdf.xacro
├── CMakeLists.txt
├── package.xml
├── README.md
└── .gitignore
```

## ⚙️ Requirements

Make sure you have:

* Ubuntu 22.04
* ROS 2 Humble
* RViz2
* Xacro
* Git

Source ROS 2 before building:

```bash
source /opt/ros/humble/setup.bash
```

## 📥 Installation

Clone the repository into your ROS 2 workspace:

```bash
cd ~/ros2_ws/src
git clone https://github.com/shwetadraut01-web/my_robot_description.git
```

Go back to the workspace:

```bash
cd ~/ros2_ws
```

## 🔨 Build

Build the package using:

```bash
source /opt/ros/humble/setup.bash
colcon build --symlink-install
```

After building, source the workspace:

```bash
source ~/ros2_ws/install/setup.bash
```

Check that ROS 2 can find the package:

```bash
ros2 pkg list | grep my_robot_description
```

Expected output:

```text
my_robot_description
```

## 🚀 Run the Robot Visualization

Launch the robot visualization:

```bash
ros2 launch my_robot_description display.launch.xml
```

RViz2 should open and display the robot model.

## 🔍 Test the Xacro File

You can verify the Xacro file independently:

```bash
ros2 run xacro xacro ~/ros2_ws/src/my_robot_de/urdf/arm.xacro
```

If the Xacro is valid, ROS 2 will generate the corresponding URDF XML output.

## 🧩 Robot Model

The robot is constructed from multiple links connected using joints.

The model includes components such as:

* Base link
* Shoulder
* Arm
* Elbow
* Wrist
* Hand
* Tool

The joints define how the different parts of the robot are connected and how they can move.

## 🖥️ Visualization

The robot can be visualized using RViz2 with the provided configuration:

```text
rviz/urdf_config.rviz
```

The launch file starts the required ROS 2 nodes and loads the robot description for visualization.

## 📸 Demo

After launching:

```bash
ros2 launch my_robot_description display.launch.xml
```

RViz2 should display the robot model.

> Add a screenshot of your robot in RViz here.

For example:

```text
![Robot visualization](images/robot_rviz.png)
```

## 🔄 Updating the Repository

After making changes to the robot model:

```bash
cd ~/ros2_ws/src/my_robot_de
git add .
git commit -m "Update robot model"
git push
```

## 👩‍💻 Author

**Shweta**

GitHub:
https://github.com/shwetadraut01-web

## 📄 License

This project is currently provided for educational and development purposes.
