# Duckiebot DB21M - csc22905

This repository provides details and commands for controlling and managing the Duckiebot DB21M (named csc22905) with different tools and configurations.

## Robot Details

- **Robot Name**: csc22905
- **Dashboard**: [csc22905.local](http://csc22905.local)
- **Robot Model**: Duckiebot DB21M

## Commands used to operate the robot 

### Discover Active Duckiebots
To discover active Duckiebots on the Duckienet WiFi:
```bash
dts fleet discover
```
To safely shut down the robot:
```bash
dts duckiebot shutdown csc22905.local
```
To control the robot through the keyboard:
```bash
dts duckiebot keyboard_control csc22905
```
Pinging the Robot
- Use `ping csc22905.local` to ping the robot.
Calibration
- **Intrinsics Calibration**: Use `dts duckiebot calibrate_intrinsics csc22905` for calibrating the intrinsic parameters of the robot.
- **Extrinsics Calibration**: Use `dts duckiebot calibrate_extrinsics csc22905` for calibrating the extrinsic parameters of the robot.
Running Demos
- **Lane Following Demo**: Use `dts duckiebot demo --demo_name lane_following --duckiebot_name csc22905 --package_name duckietown_demos` to run the lane following demo.
  - Press 'a' to start the demo, 's' to stop.

GUI Tools
- Use `dts start_gui_tools csc22905` to start the GUI tools.

Building
- **Build locally**: Use `dts devel build -f` to build the project.
- **Build on the robot**: Use `dts devel build -f --arch arm32v7 -H csc22905.local` to build the project on the robot.

Docker
- Use `docker -H csc22905.local run -it --rm --net=host duckietown/mobile-robotics:v3-arm32v7` to run Docker on the robot.

Setting Parameters
- Use `rosparam set /csc22905/kinematics_node/trim 0.0916` to set the trim parameter.

Custom Script
- Hello from `My_Robot` code located in `packages/my_package/my_script.py`.

