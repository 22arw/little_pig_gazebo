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

### Using Laser/Camera with RVIZ/Gazebo

Before launching Gazebo, you will need to open another terminal tab and run the following command:

- ```rosrun tf static_transform_publisher 0 0 0 0 0 1 map basic_laser_pig/laser_link 100```

Similarly, you will need a statis transform publisher for the camera:

- ```rosrun tf static_transform_publisher 0 0 0 0 0 1 map basic_laser_pig/laser_link 100```

Run this command to launch little pig laser in the gas station simulation

- ```roslaunch little_pig_gazebo gas_station.launch```

You are able to add laser pig to any simulation by making sure the Launch File's param "Robot Description" is set to find basic_laser_pig 

Now, you can launch Gazebo and RVIZ. Inside of RVIZ, add the laser component to the displays with the LaserScan topic set to /basic_laser_pig/laser_link. Also check the Global Options to ensure the fixed frame is set to map. After that, you can similarly add the camera data.

### Troubleshooting

If you get stuck in Gazebo attempting to open the laser pig simulation, try simply opening the ```basic_pig_gz.launch``` file first. I'm not sure why this happens, but this is a workaround.