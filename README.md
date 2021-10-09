# udm_sungkur_gb

This Repository contains only Part 1 of the project.
1) urdf_quad contain the details about the robot Quad (only one leg).
2) udm_oneleg_moveit is generated with moveit.
3) udm_project_control consist of node to control the robot direct or inverse.

## Installation
The package need to be install in your catkin workspace.
```
cd catkin_ws/src
git clone https://github.com/Seekcha/udm_sungkur_gb.git
catkin build
cd ..
source devel/setup.bash
```

## Execution
Open world.launch in first terminal:
```
source devel/setup.bash
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

Open world.launch in second terminal:
```
source devel/setup.bash
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml

```

Open world.launch in third terminal:
```
source devel/setup.bash
export TURTLEBOT3_MODEL=waffle_pi
rosrun udm_sungkur_gb global_localization.py

```
