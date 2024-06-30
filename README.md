# ros2_amr
ros2_project


## Launch the robot inside gazebo world
```
ros2 launch bumperbot_description gazebo.launch.py world_name:=small_house
```
## Run the robot terminal
```
ros2 topic pub /bumperbot_controller/cmd_vel_unstamped geometry_msgs/msg/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.5" --rate 20

```

## Run the robot using teleop_twist_keyboard
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args --remap /cmd_vel:=/bumperbot_controller/cmd_vel_unstamped
```
