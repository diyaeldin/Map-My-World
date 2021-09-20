# Map My World

Final Map can be found here: https://drive.google.com/file/d/1K2Dk0dEqHs8tNRavCKz1_MeDzUNTmknW/view?usp=sharing

This project is the SLAM project of the Udacity Robotics Software Engineer Nanodegree. For the project, I applied the Real-Time Appearance Based Mapping (RTAB-Map) in ROS to perform SLAM in a simulated environment. See the writeup for an extended discussion of the theoretical content on SLAM algorithms and specifics of RTAB-Map.

## Installation & Build
### ROS Kinetic
The project was developed on Ubuntu 16.04 LTS with [ROS Kinetic](http://wiki.ros.org/kinetic), [Gazebo](http://gazebosim.org/) and [catkin](http://wiki.ros.org/catkin) installed.

### Dependencies
The robot relies on the ``rtabmap_ros`` ROS package, which should be installed through ``apt-get``.

### Building the Workspace
Use ``catkin`` to build the packages from source. From the ``catkin`` workspace where you cloned the repo, run:

``catkin_make; source devel/setup.bash``

to build the workspace packages and add them to the paths of ROS.

### Running the Scripts
After the above steps, you should be able to run the commands below in separate terminals:

Launch the world in Gazebo:

``roslaunch slam_project slam_world.launch``

Launch the teleop node for keyboard control:

``roslaunch slam_project teleop.launch``

Launch the RTAB-Map mapping node

``roslaunch slam_project mapping.launch``

Launch the RViz GUI:

``roslaunch slam_project rviz.launch``
