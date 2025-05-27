ABSTRACT 
 
In the era of digital transformation, the integration of smart systems in residential environments has 
revolutionized the way we interact with our homes. This project, “SMART LIVING: RFID AND VOICE- 
CONTROLLED HOME AUTOMATION”, presents an intelligent and secure automation system using 
ESP32 microcontrollers, emphasizing user authentication, IoT-based control, and efficient energy 
management. 
The system is structured using two interconnected ESP32 modules. The primary ESP32 handles the initial 
security check through a keypad-based password mechanism. Upon correct password entry, peripheral 
sensors such as the PIR motion detector and temperature sensor are activated. If an incorrect password is 
entered, an OLED display notifies the user of a security breach, prompting a retry. Additionally, Blynk IoT 
is used to send email notifications to the user for both correct and incorrect password entries, ensuring real
time awareness of access attempts. 
 
Sensor data and control signals are transmitted to a secondary ESP32 via serial communication. This 
module manages RFID-based access control, enabling secure garage door operations through a servo motor. 
The RFID system toggles the garage door status based on recognized tags, enhancing physical access 
security. 
 
Additionally, home appliances like lights and fans are controlled via relays powered by a 12V lead-acid 
battery. The system utilizes an Arduino Bluetooth Control App on a mobile device to enable voice-based 
automation and remote switching of home loads, enhancing user convenience and smart accessibility. 
This project not only strengthens home security and automation but also showcases the seamless integration 
of multiple technologies using RFID, voice control, sensors, and IoT into a compact, user-friendly smart 
living solution.

	ORGANISATION OF THE PROJECT:

The project is organized into several key modules, each addressing a specific functionality:

1.	Security and Sensor Activation
•	A keypad is connected to the primary ESP32, where the user must input a password.
•	Incorrect password attempts are flagged as a security breach on the OLED display.
•	On successful authentication, PIR motion and temperature sensors are activated.
•	An automatic email is sent to the user each time a password is entered on the keypad—whether correct or incorrect. This feature, implemented using Blynk IoT, keeps the user informed in real-time about successful logins or potential unauthorized access attempts, thereby enhancing the overall security of the system.

2.	Inter-ESP32 Communication
•	Serial communication is used to transfer sensor and control data between two ESP32 microcontrollers to divide processing and control tasks efficiently.

3.	Access Control with RFID
•	An RFID module connected to the second ESP32 controls a servo motor to open/close a garage door based on tag authentication.

4.	Load Control and Automation
•	Lights and fans are operated via relay modules connected to a 12V lead-acid battery.
•	System status and control are accessible through an OLED display for real-time updates.

5.	IoT and Voice Control Integration
•	A web dashboard is created using the Arduino Bluetooth app for remote monitoring.
•	Voice commands are integrated to control home appliances, enhancing user interaction.

SYSTEM OVERVIEW/ BLOCK DIAGRAM

![image](https://github.com/user-attachments/assets/27ca1095-fdb2-451e-8b9e-830974667e9a)


Fig.1 Block diagram

RESULTS AND DISCUSSION:

The implementation of the SMART LIVING system successfully achieved secure and intelligent home automation using ESP32 microcontrollers. The integration of a keypad-based password system effectively restricted unauthorized access, with real- time OLED feedback enhancing usability. Upon successful authentication, the motion and temperature sensors were activated, enabling automated responses such as alerting via buzzer or environmental monitoring. The RFID-based garage system operated reliably, allowing smooth control of the servo motor for gate operation. Voice commands through the Blynk IoT platform functioned seamlessly, allowing remote and real-time control of home appliances like lights and fans via relay modules. The system demonstrated stable serial communication between the two ESP32s, ensuring synchronized operations. Overall, the project confirmed the feasibility and effectiveness of combining IoT, RFID, and voice control technologies for a modern smart living environment.
 

 ![image](https://github.com/user-attachments/assets/b92e3696-1bf5-4e39-bfad-1438d84d67d8)

Fig.3 Overall setup


![image](https://github.com/user-attachments/assets/c110f9cf-914b-4dbf-bd7d-700c7524ace0)


Fig.4 Relay and keypad connection


![image](https://github.com/user-attachments/assets/d263b9d6-c778-4c82-be39-cf9670616cf0)
 

Fig 5: Email Alert Triggered on Incorrect Password Entry


 ![image](https://github.com/user-attachments/assets/3352d6ed-d125-4288-928e-b9f349e3d209)


Figure 6 :Email Notification on Correct PIN Entry

![image](https://github.com/user-attachments/assets/cfd53347-6832-4c84-bd16-5b92cf868791)

 
Figure 7: Arduino-Based Mobile App for Remote Switching of Home Appliances


 ![image](https://github.com/user-attachments/assets/981dcb6e-b764-40e0-942a-f6db11421985)

Figure 8: Arduino-Based Bluetooth App Interface for Voice Command Control 

CONCLUSION;

The Smart Living: RFID and Voice-Controlled Home Automation system demonstrates a practical and efficient solution for enhancing residential security and convenience. The system achieves multi-layered control and monitoring by integrating keypad authentication, motion and temperature sensing, RFID-based access, and voice-controlled IoT functionalities using ESP32 microcontrollers. The successful coordination between hardware components and wireless communication showcases the potential of low-cost, scalable home automation systems. This project not only improves user experience through automation and security but also promotes energy efficiency and remote accessibility, making it a step forward toward future smart home technologies.

