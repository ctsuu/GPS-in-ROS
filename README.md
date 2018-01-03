# GPS-in-ROS
Install GPS in ROS environment

## Create ROS carkin workspace
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
-- The C compiler identification is GNU 5.4.0
-- The CXX compiler identification is GNU 5.4.0
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Using CATKIN_DEVEL_PREFIX: /home/rainbow/catkin_ws/devel
-- Using CMAKE_PREFIX_PATH: /opt/ros/kinetic
-- This workspace overlays: /opt/ros/kinetic
-- Found PythonInterp: /usr/bin/python (found version "2.7.12") 
-- Using PYTHON_EXECUTABLE: /usr/bin/python
-- Using Debian Python package layout
-- Using empy: /usr/bin/empy
-- Using CATKIN_ENABLE_TESTING: ON
-- Call enable_testing()
-- Using CATKIN_TEST_RESULTS_DIR: /home/rainbow/catkin_ws/build/test_results
-- Looking for pthread.h
-- Looking for pthread.h - found
-- Looking for pthread_create
-- Looking for pthread_create - not found
-- Looking for pthread_create in pthreads
-- Looking for pthread_create in pthreads - not found
-- Looking for pthread_create in pthread
-- Looking for pthread_create in pthread - found
-- Found Threads: TRUE  
-- Found gtest sources under '/usr/src/gtest': gtests will be built
-- Using Python nosetests: /usr/bin/nosetests-2.7
-- catkin 0.7.8
-- BUILD_SHARED_LIBS is on
-- Configuring done
-- Generating done
-- Build files have been written to: /home/rainbow/catkin_ws/build
####
#### Running command: "make -j8 -l8" in "/home/rainbow/catkin_ws/build"
####
rainbow@rainbow-T3500:~/catkin_ws$ ls
build  devel  src
~~~

