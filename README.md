# gazebo_simulation

This package will start the gazebo designed world with the simulated 2 wheel robot.

The robot is equipted with a stereo camera, 2D lidar and can provide wheels odometry.

## Dependencies

```
sudo apt install ros-melodic-gazebo-ros
sudo apt install ros-melodic-teleop-twist-keyboard
sudo apt install ros-melodic-joint-state-publisher
sudo apt install ros-melodic-dynamic-robot-state-publisher
sudo apt install ros-melodic-xacro
```

## Ho to use:

Currently our repositoy depends on other git repository.
So make sure that in your catkin workspace has the following packsge: 
realsense_gazebo_plugin 

```
mkdir -p ~/catkin_ws/src && cd ~/catkin_ws/src
git clone https://github.com/project-omicron/gazebo_simulation.git
git clone https://github.com/SyrianSpock/realsense_gazebo_plugin.git
cd ../
catkin_make
source devel/setup.bash
roslaunch gazebo_simulation world.launch
```

Currently we have an empty world.

## How to run the robot in the simulated environment:

Open the new terminal window and run:
```
cd ~/catkin_ws/ && source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

