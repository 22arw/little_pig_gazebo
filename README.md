# Little Pig Gazebo - ROS Package

This repository is meant for all the simulation based code **only**. Example's of such:
- Creating a different type of launch file that would spawn Basic Pig into other simulation environments
- Launching Basic Pig with other simulated gear.

### Installation instructions

Heres a simple guide to get you started with Little Pig Gazebo. Before continuing, be sure to have ROS Melodic installed.

- **Step 1.**
  - ```cd catkin_ws/src```
- **Step 2.**
  - ```git clone https://github.com/22arw/little_pig_gazebo.git```
  - If you don't have the other three packages you can run these lines also:
    - ```git clone https://github.com/22arw/little_pig_ctrl.git```
    - ```git clone https://github.com/22arw/little_pig_rviz.git```
    - ```git clone https://github.com/22arw/little_pig_description.git```

Your resulting directory should have this layout:

- catkin_ws/
  - src/
    - little_pig_ctrl/
    - little_pig_description/
    - little_pig_gazebo/
    - little_pig_rviz/

### Usage Instructions

Once you have this repo downloaded, run the following commands in the terminal:

- ```cd ..```
- ```catkin_make```

This should completed without failing. If it does fail, call Coach. From the ```catkin_ws/``` directory run this:

- ```roslaunch little_pig_gazebo basic_pig_gz.launch```

You should see a gazebo window open with an empty world and Basic Pig just sitting there. If it fails, Call Coach.
