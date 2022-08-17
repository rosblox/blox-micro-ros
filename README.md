# BloX micro-ROS

The BloX micro-ROS communicates with micro controllers using [micro-ROS](https://micro.ros.org/). It is an advanced ROSbloX module and requires the user to install additional software on their computer and implement/build/upload code to their micro controllers.

## Data

The BloX micro-ROS publishes data according to the code run on the micro controller.

## Programming a Teensy with micro-ROS in the Arduino IDE

Works for all Teensies supported by micro-ROS -> [Supported Hardware](https://micro.ros.org/docs/overview/hardware/).

1. Install [Arduino IDE](https://docs.arduino.cc/software/ide-v1)
2. Install [Teensyduino add-on](https://www.pjrc.com/teensy/td_download.html) for the Arduino IDE
3. Install the micro-ROS library in the Arduino IDE by  
    a) downloading its latest [release](https://github.com/micro-ROS/micro_ros_arduino/releases) and  
    b) including it in your project using `Sketch -> Include library -> Add .ZIP Library...`
4. Patch Teensyduino to work with micro-ROS library  
    a) Go to Arduino + Teensyduino installation folder `cd $ARDUINO_PATH/hardware/teensy/avr/`  
    b) Replace platform.txt `curl https://raw.githubusercontent.com/micro-ROS/micro_ros_arduino/main/extras/patching_boards/platform_teensy.txt > platform.txt` 
5. Compile and upload one of the micro-ROS examples.  
   Note, they are listed as incompatible, but work.


## More information
https://github.com/micro-ROS/micro_ros_arduino  
https://micro.ros.org/docs/tutorials/core/teensy_with_arduino/