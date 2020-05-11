# Little Pig Gazebo - ROS Package

### Using Laser/Camera with RVIZ/Gazebo

You are able to add laser pig to any simulation by making sure the Launch File's param "Robot Description" is set to find basic_laser_pig 

Now, you can launch Gazebo and RVIZ. Inside of RVIZ, add the laser component to the displays with the LaserScan topic set to /basic_laser_pig/laser_link. Also check the Global Options to ensure the fixed frame is set to map. After that, you can similarly add the camera data.
