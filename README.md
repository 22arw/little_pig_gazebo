# Little Pig Gazebo - ROS Package

## Overview

This repository has the files necessary for the Gazebo part of the simulation. [Gazebo](http://gazebosim.org/) is the simulation software used to virtually test the little pig robot.  The config and launch files in this repository are called as part of full.launch in [little_pig_ctrl](https://https://github.com/22arw/ackermann_controller). 

## Contents

#### config 
	gazebo_controller_gains.yaml has the PID controller gains for simulated robot in Gazebo. These are only used in Gazebo.

#### launch
	Launch file used is simulation.launch. This should not be launched on its own and should be launched through full.launch in the little_pig_ctrl folder with sim set to true. Otherwise, it will fail to start.

#### worlds
	These are all the worlds that can be loaded into the simulation. The world that the launch file loads can be changed in full.launch by changing the argument "world_name" to the world's filename minus the file extension (for example, gas_station). This does mean all world files must have the file extension .world.

## Using Laser/Camera with RVIZ/Gazebo

You are able to add laser pig to any simulation by making sure the Launch File's param "Robot Description" is set to find basic_laser_pig 

Now, you can launch Gazebo and RVIZ. Inside of RVIZ, add the laser component to the displays with the LaserScan topic set to /basic_laser_pig/laser_link. Also check the Global Options to ensure the fixed frame is set to map. After that, you can similarly add the camera data.
