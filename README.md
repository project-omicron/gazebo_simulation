# gazebo_simulation

This package will start the gazebo designed world with the simulated 2 wheel robot.

The robot is equipped with a stereo camera, 2D lidar and can provide wheels odometry.

## Dependencies

### Basic```
sudo apt install ros-melodic-gazebo-ros
sudo apt install ros-melodic-teleop-twist-keyboard
sudo apt install ros-melodic-joint-state-publisher
sudo apt install ros-melodic-dynamic-robot-state-publisher
sudo apt install ros-melodic-xacro
sudo apt install ros-melodic-rviz
sudo apt install ros-melodic-compressed-image-transport
sudo apt install ros-melodic-theora-image-transport
sudo apt install ros-melodic-camera-info-manager

### SLAM
sudo apt install ros-melodic-cartographer ros-melodic-cartographer-ros ros-melodic-cartographer-rviz


## How to use

To give gazebo ability to find our models, substitute your_catkin_ws_path with real value and add the resulting line to .bashrc:
```
export GAZEBO_MODEL_PATH=your_catkin_ws_path/src/gazebo_simulation/models:$GAZEBO_MODEL_PATH
``` 

Currently our repository depends on other git repository.
So make sure that in your catkin workspace has the following package: 
realsense_gazebo_plugin 

```
mkdir -p ~/catkin_ws/src && cd ~/catkin_ws/src
git clone https://github.com/project-omicron/gazebo_simulation.git
git clone https://github.com/SyrianSpock/realsense_gazebo_plugin.git
cd ../
catkin_make
source devel/setup.bash
```

To launch an empty world, use command
```
roslaunch gazebo_simulation world.launch
```

Alternatively to launch the world only with linoleum tiles on arena, use command
```
roslaunch gazebo_simulation world_of_arena.launch
```

Or to launch the world with linoleum tiles and labyrinth, use command
```
roslaunch gazebo_simulation world_of_labyrinth.launch
``` 

## How to run the robot in the simulated environment

Open the new terminal window and run:
```
cd ~/catkin_ws/ && source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
