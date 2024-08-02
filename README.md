# Launch-TurtleBot-navigation

## Install ROS on Remote PC
Open the terminal with Ctrl+Alt+T and enter below commands one at a time.
In order to check the details of the easy installation script, please refer to the script file.
```
$ sudo apt-get update
$ sudo apt-get upgrade
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh
$ chmod 755 ./install_ros_kinetic.sh 
$ bash ./install_ros_kinetic.sh
```
<img width="580" alt="1 1 1" src="https://github.com/user-attachments/assets/8016a245-5534-4cfa-83c7-a2024967b4ce">
<img width="929" alt="1 3" src="https://github.com/user-attachments/assets/c8b657af-6881-4578-b529-ed6d425d90f2">
![Screenshot 2024-08-02 231854](https://github.com/user-attachments/assets/89a41621-a737-46fc-a8f9-0427a9084c91)
![shm](https://github.com/user-attachments/assets/5ba6456a-0449-4fb5-a54a-b42e11563073)

 ##  Install Dependent ROS Packages
## NOTE: ## it is important to install
 ~~~
$ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy \
  ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc \
  ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan \
  ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python \
  ros-kinetic-rosserial-server ros-kinetic-rosserial-client \
  ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server \
  ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro \
  ros-kinetic-compressed-image-transport ros-kinetic-rqt* \
  ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
~~~

<img width="917" alt="1 4" src="https://github.com/user-attachments/assets/c962ab90-bcb1-416c-b112-18f700a56792">

## Install TurtleBot3 Packages
Install TurtleBot3 via Debian Packages.
~~~
$ sudo apt-get install ros-kinetic-dynamixel-sdk
$ sudo apt-get install ros-kinetic-turtlebot3-msgs
$ sudo apt-get install ros-kinetic-turtlebot3
~~~

<img width="923" alt="1 5" src="https://github.com/user-attachments/assets/c20b53db-3ada-471d-965f-4656fa1f6f20">
<img width="928" alt="1 6" src="https://github.com/user-attachments/assets/769d8dc9-9c65-418c-bb19-60ee790d08ae">
<img width="917" alt="1 7" src="https://github.com/user-attachments/assets/f847738a-4b9d-4941-8f7e-ac00c057325b">

## Install Simulation Package
The TurtleBot3 Simulation Package requires turtlebot3 and turtlebot3_msgs packages as prerequisite. Without these prerequisite packages, the Simulation cannot be launched.
Please follow the PC Setup instructions if you did not install required packages and dependent packages.

~~~
$ cd ~/catkin_ws/src/
$ git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
~~~
<img width="670" alt="1 8" src="https://github.com/user-attachments/assets/fe482e62-0ac0-4ce9-bc93-c5c4ab6f9bb2">

##Launch Simulation World
Three simulation environments are prepared for TurtleBot3.I selected TourtleBot3World
~~~
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
~~~
<img width="710" alt="1 9" src="https://github.com/user-attachments/assets/43456ff9-0926-40ca-a0f3-a56167c18eda">

<img width="923" alt="1 10" src="https://github.com/user-attachments/assets/3fe8d6d5-226d-47d8-bffd-909e09127dca">
![Screenshot 2024-08-02 202445](https://github.com/user-attachments/assets/efb6037a-9b11-4297-a805-60347618eca9)
![Screenshot 2024-08-02 202445](https://github.com/user-attachments/assets/efb6037a-9b11-4297-a805-60347618eca9)
