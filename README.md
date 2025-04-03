# Lab-8-Report

**Names of People Involved (Group Members):**  
Faith Cox & Quinn Rison 

**Date Submitted:**  
4/2/2025

---

## Introduction / Summary

This lab aims to introduce a straightforward method for developing mobile applications, using the example of a remote control for the SparkFun Robot car. The Android system's open nature facilitates broad participation, contrasting with Apple's stringent app store review process. Google's App Inventor, initially created to enable app development by school children, exemplifies this inclusivity and is now managed by MIT, with limited support for iPhones. Additionally, the lab explores Bluetooth technology, a widely used standard for short-range communication operating at 2.4GHz, highlighting its ease of programming and cost-effectiveness. Bluetooth modules will be utilized to replace USB wiring as the communication medium.

---

## Methods / Tests

To begin, a computer capable of running Arduino IDE and Chrome Browser is required, along with a smartphone operating on Android OS with the MIT AI2 Companion app installed. The SparkFun Inventor’s kit, which includes the RedBoard, ultrasonic sensor, two motors, motor driver, and battery pack, is essential. Additionally, a cable or adaptor to connect the smartphone to the RedBoard and an HC-05 Bluetooth UART Module are necessary components.
The first part of the lab involves assembling and testing the robot. The wheels should be attached to the motors used in Lab 6, and the wheel/motor assembly must be connected to the chassis with careful alignment. The robot's movement—forward, backward, right, and left—should be verified by sending commands via serial communications using the Arduino IDE Serial Monitor. The battery pack should be positioned on the bottom of the robot to avoid contact with the floor when the binder clip is installed. It is important to determine the minimum speed required to move the complete car, considering the findings from Lab 6 regarding motor speed.

**PHOTO OF CAR ABOVE**
The second part focuses on developing the app. An account should be created and logged into the App Inventor 2 web-based tool. A new project should be started with a descriptive name that includes team members' names. In the Designer environment, a button to initialize serial communications, a label to display communication strings received from the Arduino, and user interface objects to control the car (forward, backward, right, left at three different speeds) should be added. Additionally, a Serial component from the Connectivity section and a Clock component from the Sensors section are required. In the Blocks environment, blocks should be added to establish communications after pressing the serial communications button. The block “call serialObject.WriteSerial.data” and a regular “text” block should be used to send commands to the RedBoard. The app should be built (Build > Android App (.apk)), installed on the phone using the QR code, and tested with a USB-C to USB-A adapter and Arduino cable.
The final part involves creating a wireless remote. The HC-05 module should be wired on the breadboard using pins 2 and 3 for Rx and Tx, including a 1kΩ-2kΩ voltage divider. The Arduino sketch should be modified by including specific code lines before the setup function, adding code lines inside the setup function, replacing the conditional inside the loop function, and adding functions at the end of the sketch. A copy of the previous app should be saved in App Inventor 2 with a descriptive name. In the Designer environment, the BluetoothClient from the Connectivity section, ListPicker and Label objects from the User Interface section, and the GetApiLevel extension from the Instructor’s GitHub account should be added. The TinyDB from the Storage section is also required. In the Blocks environment, the “call serialobject.WriteSerial” blocks should be replaced with “call BluetoothClient.SendText” blocks, including the new line command “/n”.



---

## Results
shown below is a screenshot of the app created on MIT App Inventor for this lab. It displays the programmed buttons.

<p align="center">
  <img src="" width="500">
  <br>
  <b>Figure 1:</b> MEASURING TRUE RESISTOR MEASUREMENTS
</p>


---

## Discussion
**Discussion Question 1: In Lab 6 we found out what was the minimum speed that will move the motors. What is the minimum speed that will move the complete car?**

Minimum speed to move the car forward was 105 on Arduino IDE. We achieved this value by changing the “slow_speed” variable within our program. We tested several values but concluded on this one as the vehicle remained in motion the entire time. 


---

## Conclusion




**Citations**

Copilot. (2025). Summary of the introduction, easy app development, and bluetooth. Retrieved from [Quinn’s conversation with Copilot].

Copilot. (2025). Methods for Assembling and Controlling a SparkFun Robot Car Using App Inventor and Bluetooth. Retrieved from [Quinn’s conversation with Copilot].

---

*End of Lab Report*
