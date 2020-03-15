# gazebo_simulation

This package will start the gazebo designed world with the simulated 2 wheel robot.

The robot is equipted with a stereo camera, 2D lidar and can provide wheels odometry.

## Dependencies

```
sudo apt install ros-melodic-teleop-twist-keyboard
sudo apt install ros-melodic-joint-state
sudo apt install ros-melodic-dynamic-robot-state-publisher-publisher
sudo apt install ros-melodic-xacro
```

## Ho to use:

```
mkdir -p ~/catkin_ws/src && cd ~/catkin_ws/src
git clone https://github.com/project-omicron/gazebo_simulation.git
cd ../
catkin_make
source devel/setup.bash
roslauch gazebo_simulation world.launch
```

Currently we have an empty world.

## How to run the robot in the simulated environment:

Open the new terminal window and run:
```
cd ~/catkin_ws/ && source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

