# udm_sungkur_gb
Ce package contient le package de la question 5 pour la partie 2 du TP4 Il permet de localiser le robot en faisant appel au service \global_localization et \request_nomotion_update
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
