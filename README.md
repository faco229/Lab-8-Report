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

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/Completed%20Car.jpg" width="500">
  <br>
  <b>Figure 1:</b> Completed car build with Bluetooth connection to app
</p>

The second part focuses on developing the app. An account should be created and logged into the App Inventor 2 web-based tool. A new project should be started with a descriptive name that includes team members' names. In the Designer environment, a button to initialize serial communications, a label to display communication strings received from the Arduino, and user interface objects to control the car (forward, backward, right, left at three different speeds) should be added. Additionally, a Serial component from the Connectivity section and a Clock component from the Sensors section are required. In the Blocks environment, blocks should be added to establish communications after pressing the serial communications button. The block “call serialObject.WriteSerial.data” and a regular “text” block should be used to send commands to the RedBoard. The app should be built (Build > Android App (.apk)), installed on the phone using the QR code, and tested with a USB-C to USB-A adapter and Arduino cable.
The final part involves creating a wireless remote. The HC-05 module should be wired on the breadboard using pins 2 and 3 for Rx and Tx, including a 1kΩ-2kΩ voltage divider. The Arduino sketch should be modified by including specific code lines before the setup function, adding code lines inside the setup function, replacing the conditional inside the loop function, and adding functions at the end of the sketch. A copy of the previous app should be saved in App Inventor 2 with a descriptive name. In the Designer environment, the BluetoothClient from the Connectivity section, ListPicker and Label objects from the User Interface section, and the GetApiLevel extension from the Instructor’s GitHub account should be added. The TinyDB from the Storage section is also required. In the Blocks environment, the “call serialobject.WriteSerial” blocks should be replaced with “call BluetoothClient.SendText” blocks, including the new line command “/n”.



---

## Results
Shown below is a screenshot of the app created on MIT App Inventor for this lab. It displays the programmed buttons.

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/app%20ss.png" width="500">
  <br>
  <b>Figure 2:</b> Screenshot of the app interface
</p>

It is important to note that the app was not entirely compatible IOS devices. The lab instructor was able to connect an Android device to ensure the designed app worked properly. 

The app was coded on MIT App Inventor using various coding blocks shown below. In addition, this block method was used to connect the program, mobile device, and car all together. 

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/PROGRAMMINGBLOCKS.png" width="500">
  <br>
  <b>Figure 3:</b> Blcok coding part 1
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/PROGRAMMINGBLOCKS2.png" width="500">
  <br>
  <b>Figure 4:</b> Blcok coding part 2
</p>

An integral part of this lab was editing the code to connect the car to the app via bluetooth. In addition, various changes were made to the code (see the beginning of the methods section). Below is the full, edited, and completed code for this lab.

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE1.png" width="500">
  <br>
  <b>Figure 5:</b> Arduino IDE Code Part 1
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE2.png" width="500">
  <br>
  <b>Figure 6:</b> Arduino IDE Code Part 2
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE3.png" width="500">
  <br>
  <b>Figure 7:</b> Arduino IDE Code Part 3
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE4.png" width="500">
  <br>
  <b>Figure 8:</b> Arduino IDE Code Part 4
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE5.png" width="500">
  <br>
  <b>Figure 9:</b> Arduino IDE Code Part 5
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE6.png" width="500">
  <br>
  <b>Figure 10:</b> Arduino IDE Code Part 6
</p>

<p align="center">
  <img src="https://github.com/faco229/Lab-8-Report/blob/main/CODE7.png" width="500">
  <br>
  <b>Figure 11:</b> Arduino IDE Code Part 7
</p>

---

## Discussion
**Discussion Question 1: In Lab 6 we found out what was the minimum speed that will move the motors. What is the minimum speed that will move the complete car?**

Minimum speed to move the car forward was 105 on Arduino IDE. We achieved this value by changing the “slow_speed” variable within our program. We tested several values but concluded on this one as the vehicle remained in motion the entire time. 


---

## Conclusion


This lab successfully demonstrated how to integrate hardware and software by building a functional Bluetooth-controlled robot car using the SparkFun kit and MIT App Inventor. Through hands-on assembly, programming, and wireless connectivity, we explored the fundamentals of mobile app development and embedded systems. Despite compatibility limitations with iOS, the Android-based app effectively communicated with the car via the HC-05 Bluetooth module, allowing real-time directional control. This project emphasized the importance of iterative testing and troubleshooting, as we adjusted code and hardware connections to optimize performance. Overall, the lab provided a practical introduction to mobile-driven robotics and reinforced key engineering skills in problem-solving and system integration.



**Citations**

Copilot. (2025). Summary of the introduction, easy app development, and bluetooth. Retrieved from [Quinn’s conversation with Copilot].

Copilot. (2025). Methods for Assembling and Controlling a SparkFun Robot Car Using App Inventor and Bluetooth. Retrieved from [Quinn’s conversation with Copilot].

ChatGPT. (2025). Conclusion section for Lab 8 Report: Bluetooth-Controlled Robot Car using MIT App Inventor. OpenAI. https://chat.openai.com/

---

*End of Lab Report*
