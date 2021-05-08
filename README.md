# sbot
This is a simple robot for making simulations and perform various experiments

## Dependencies
- https://github.com/nilseuropa/realsense_ros_gazebo


## Instructions

>To spawn the bot in gazebo:

```
roslaunch sbot_description gazebo.launch
```
>To launch the bot in rviz:

```
roslaunch sbot_descriiption display.launch
```

> office World 

```bash
roslaunch sbot_description office_gazebo.launch
```

> Run Gmapping

```bash
roslaunch sbot_description office_gazebo.launch

roslaunch sbot_nav gmapping.launch

# to save map
rosrun map_server map_saver -f map

```

> Run Localization

```bash
roslaunch sbot_description office_gazebo.launch

roslaunch sbot_nav map_server.launch

roslaunch sbot_nav amcl.launch

```

> Run Navigation

```bash
roslaunch sbot_description office_gazebo.launch

roslaunch sbot_nav map_server.launch

roslaunch sbot_nav amcl.launch

roslaunch sbot_nav move_base.launch
```
