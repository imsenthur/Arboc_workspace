# arboc_workspace
A ROS workspace with packages required for simulated control of a hyper redundant snake robot [Arboc]. 

Tested and developed with __ROS-Kinetic__ and __ubuntu 16.04__.

## Getting Started:
Clone the repository to your home directory,
```
$ git clone https://github.com/imsenthur/arboc_workspace.git
```
## Build and source:
```
$ cd arboc_workspace
$ catkin_make
$ source devel/setup.bash
```
## Make executables:
```
$ roscd snake_control/scripts/
$ sudo chmod +x gaits.py
```
## Launch Gazebo:
```
$ roslaunch snake_control gazebo.launch gait:=true
```
*If the commands are successful, gaits.py should send joint commands that cause the snake robot simulation in gazebo to start sidewinding.*

![alt text](https://raw.githubusercontent.com/imsenthur/arboc_workspace/master/arboc.png)

## Improvements:
Further modifications can be made to the hirose curve equation which serves as the source for all the joint commands generated by gaits.py inorder to model and simulate numerous gaits.

## Credits:
Credits to __Alex Ansari__ for his work on the control packages for __CMU Biorobotics Lab__'s SEA snake which served as a huge inspiration for the packages included in this workspace.
