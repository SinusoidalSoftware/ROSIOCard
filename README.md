# ROSIOCard
Sinusoidal ROSIO Card Ros Package
This package is created for [Sinusoidal ROSIO Card] (https://sinusoidal.com.tr/HenchmanRosIo/).

# Contains
This package contains software interface source and header files for Sinusoidal ROSIO Card to communicate ROS via topics.

Package contains 
- Communication Driver as hiddriver.py, 
- Hardware Interface as rosiocard.py

# Connection
Sinusoidal ROSIO Card Connection Diagram ![ROSIOConnection](https://cloud.sinusoidal.com.tr/f/cf889bc0cd134e19a84d/?dl=1)

# Requirements
  - python2 or python3 depending on ROS Melodic or Noetic
  - numpy==1.13.3
  - hidapi==0.10.1
  - udev rules
    - SUBSYSTEM=="input", GROUP="input", MODE="0666"
    - SUBSYSTEM=="usb", ATTRS{idVendor}=="0483", ATTRS{idProduct}=="5743", MODE="666", GROUP="plugdev"
    - KERNEL=="hidraw*", ATTRS{idVendor}=="0483", ATTRS{idProduct}=="5743", MODE:="0666", GROUP="plugdev"

# Installation
* Clone the repository into catkin workspace's src folder.
* catkin_make
* source devel/setup.bash
* roslaunch sinusoidal startsinusoidalrosiocard.launch

# Test 
* rosrun rviz rviz -c ultrasonic.rviz

# Screenshots
Sinusoidal ROSIO Card Rviz Scrrenshot ![RVIZScreenshot](https://cloud.sinusoidal.com.tr/f/04651a124c0347be8867/?dl=1)

