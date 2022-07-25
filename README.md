# ZS-H1B Dual H-Bridge Motor Driver #

## Installation ##

To build the contents of this package, 

    catkin_make

To install the contents of this package into an Arduino workspace, 
run the following command into the `lib` folder of the desired workspace.

    rosrun rosserial_arduino make_libraries.py ./lib motor_driver_msgs

## Truth Table ##

The following truth table covers both left and right motor movement.

|   PWM  | Direction (DIR) | Enable (En) |  Action |
|:------:|:---------------:|:-----------:|:-------:|
| 0-99 % |        1        |      1      | Forward |
| 0-99 % |        0        |      1      | Reverse |
|    0   |        X        |      1      |  Brake  |
|    X   |        X        |      0      |   Stop  |