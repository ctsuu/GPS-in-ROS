# GPS-in-ROS
Install GPS in ROS environment

## Create ROS catkin workspace
```
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/src
$ catkin_init_workspace
$ ls -l
$ cd ~/catkin_ws
$ ls -l
$ cd ~/catkin_ws
$ catkin_make
```
~~~
rainbow@rainbow-T3500:~$ mkdir -p ~/catkin_ws/src
rainbow@rainbow-T3500:~$ cd ~/catkin_ws/src
rainbow@rainbow-T3500:~/catkin_ws/src$ catkin_init_workspace
Creating symlink "/home/rainbow/catkin_ws/src/CMakeLists.txt" pointing to "/opt/ros/kinetic/share/catkin/cmake/toplevel.cmake"
rainbow@rainbow-T3500:~/catkin_ws/src$ ls -l
total 0
lrwxrwxrwx 1 rainbow rainbow 50 Jan  2 22:30 CMakeLists.txt -> /opt/ros/kinetic/share/catkin/cmake/toplevel.cmake
rainbow@rainbow-T3500:~/catkin_ws/src$ cd ~/catkin_ws
rainbow@rainbow-T3500:~/catkin_ws$ catkin_make
Base path: /home/rainbow/catkin_ws
Source space: /home/rainbow/catkin_ws/src
Build space: /home/rainbow/catkin_ws/build
Devel space: /home/rainbow/catkin_ws/devel
Install space: /home/rainbow/catkin_ws/install
####
#### Running command: "cmake /home/rainbow/catkin_ws/src -DCATKIN_DEVEL_PREFIX=/home/rainbow/catkin_ws/devel -DCMAKE_INSTALL_PREFIX=/home/rainbow/catkin_ws/install -G Unix Makefiles" in "/home/rainbow/catkin_ws/build"
####

####
#### Running command: "make -j8 -l8" in "/home/rainbow/catkin_ws/build"
####
rainbow@rainbow-T3500:~/catkin_ws$ ls
build  devel  src
~~~
## Install GPS Driver
```
$ cd ~/catkin_ws/src/
$ git clone https://github.com/ros-drivers/nmea_navsat_driver -b jade-devel
$ cd ..
$ catkin_make
$ catkin_make install
$ source devel/setup.bash
```
## Testing the GPS


```
$ ls -l /dev/ttyU*
crw-rw---- 1 root dialout 188, 0 Jun 12 13:28 /dev/ttyUSB0
$ sudo usermod -a -G dialout [user]
$ sudo chmod 666 /dev/ttyUSB0
to add 'rw_' for all users.

$ rosrun nmea_navsat_driver nmea_serial_driver _port:=/dev/ttyUSB0 fix:=/gps/fix
```
In new terminal 
```
$ rostopic list
/gps/fix
$ rostopic echo /gps/fix
header: 
  seq: 323
  stamp: 
    secs: 1514960246
    nsecs: 460407972
  frame_id: "/gps"
status: 
  status: 0
  service: 1
latitude: 51.0330016667
longitude: -114.179218333
altitude: 1196.7
position_covariance: [1.44, 0.0, 0.0, 0.0, 1.44, 0.0, 0.0, 0.0, 5.76]
position_covariance_type: 1
---
```
It works.



