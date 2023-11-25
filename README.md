# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:

Initiate the MobileRobot.

### Step2:

Connect your PC with the MobileRobot.

### Step3:

Program the movements of the robot using python code

### Step4:

Execute the python program.

## Program:
```
### developed by : SUBALAKSHMI.S
### register number :212222100051
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=128,effect="on")

    ep_chassis.move(x=0.5,y=0,z=85,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=153,effect="on")

    ep_chassis.move(x=0.95,y=0,z=0,xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")
    
    ep_chassis.move(x=0,y=-1.3,z=0,xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-125, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")

    ep_chassis.move(x=-1.65, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=102,b=255,effect="on")

    ep_chassis.move(x=0, y=1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=85, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
   
```

## MobileRobot Movement Image:

![image](https://github.com/Subalakshmisuresh/mobilerobot-openloopcontrol/assets/121957896/e78254a6-46c3-4600-9300-0755a06a41d0)

![image](https://github.com/Subalakshmisuresh/mobilerobot-openloopcontrol/assets/121957896/db446af8-de99-4d4d-b52d-c22144c3f6c4)


## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


