# Installing-ROS-On-Ubunu-Jetson-Nano

Task 1 (ROS Installation ) repository for the smart methods summer training 
The steps that you need to start with  
1) Download the virtual box  
2) Decide which ROS type you want ( Kinetic , Melodic etc… ) (in this case I chose melodic 
3) Download the suitable ubuntu suitable for melodic (18.04.5) 
4) Download ROS ( melodic type )  
5) Download RVIZ and run it  
Where to install the Virtual Box :  
https://www.virtualbox.org/wiki/Downloads 
Where to install the ubuntu 18.04.5 :  
https://www.virtualbox.org/wiki/Downloads 
the Melodic ROS download instructions link :  
http://wiki.ros.org/ROS/Installation 
-During the selection avoid windows and choose LINUX instead  
Instructions on the melodic arm is linked and they were taken from the smart methods :  
https://github.com/smart-methods/arduino_robot_arm 
 
NOTES ON THE sudo nano ~/.bashrc COMMAND : 
Scroll to the end of the page and name your system I want mine to reemaalmurayshid so mine will look like this :  
source /home/reemaalmurayshid/catkin_ws/devel/setup.bash 
Once you finish press the following buttons  
1)CTRL+O  
2)ENTER  
3)CTRL + X 
Then write the source command :  
source ~/.bashrc 
to launch the ROS use this command :  
roslaunch robot_arm_pkg check_motors.launch


------------------------------------------------------------------------------------------------------------------------------------------------------------------
The second task is the installing of ROS on jetson nano steps  
Disclaimer :  
All of the commands were taken from this link :  
https://github.com/AnbuKumar-maker/ROS-Installation-on-Jetson-Nano/tree/m 
 
Now the steps and commands go as follows :  
1) Install the package  
sudo sh -c 'echo "deb  http://packages.ros.org/ros/ubuntu  $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list 
 
2) Put the package key  
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654 
 
3) Update the package  
sudo apt update 
 
4) Install Melodic ROS  
sudo apt install ros-melodic-desktop 
 
5) ROS initiation  
sudo rosdep init 
 
6) Update your ROS  
rosdep update 
 
7) Get the source of the ROS Melodic  
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashr 
 
8) Confirm the source  
source ~/.bashrc 
 
9) Make sure of the type by using this command 
rosversion -d
