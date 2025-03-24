# 🚁 Mutlirotor-Quadcopter-using-KK2.1.5-Flight-Controller- 🛰🎯
Project on buidling a Quadcopter

## Overview / Project Description 🔎📝
This project involves designing and developing a **multirotor quadcopter** for aerial applications, leveraging the **KK2.1.5 Flight Controller**. The quadcopter supports **wireless telemetry**, **real-time monitoring**, and **autonomous stabilization**.
The motivation behind utilizing drones equipped with the KK2.1.5 flight controller and FSi6 
6-channel transmitter lies in their ability to address these challenges effectively. This 
combination offers a balance of affordability, stability, and precise control, making it 
accessible to a broader audience, including hobbyists, educators, and professionals. By leveraging this setup, users can explore innovative applications such as crop monitoring, disaster assessment, and educational training, thereby enhancing productivity and reducing operational costs. This approach not only democratizes drone technology but also encourages creativity and problem-solving across 
various fields.

## Features 🧩
- 6-channel transmitter-based control
- ESC and BLDC motor calibration using **MultiWii firmware**
- Wireless telemetry integration for real-time diagnostics
- Optimized stability and responsiveness

## Components Used ⚙️
- Flight Controller
- 6 Channel Transmitter & Receiver
- Brushless DC Motors (1000 kv)
- Propellers
- Drone Body
- ESC (Electronic Speed Controllers)
- PDB (Power Distribution Board)
- LiPo Batteries (Lithium Polymer)

## Technologies Used 🦾
- **Microcontroller:** KK2.1.5 Flight Controller
- **Programming:** C/C++, Arduino (for testing purpose: ESC's and BLDC motors using Arduino) 
- **Tools:** MultiWii, Mission Planner

## Working 👩🏻‍💻📓✍🏻💡
**WORKING OF THE SYSTEM** 

The system consists of two main units: the transmitter unit, and the receiver unit, 
which is mounted on the drone. The transmitter unit consists of a controller which is 
FLYSKY FS-i6 6-channel 2.4GHz transmitter includes  
Channels 1-4 (Main Controls): 
Channel 1: Ailerons (roll control)  
Channel 2: Elevator (pitch control)  
Channel 3: Throttle (power control)  
Channel 4: Rudder (yaw control)  
 
Channels 5-6 (Auxiliary Functions): 
Channel 5: Often used for flaps or gear, depending on the model setup.  
Channel 6: Can be used for flight modes, gyro gain, or other functions.   
while the receiver unit on the drone comprises an Flight Controller KK2.1.5, a FLYSKY FS
iA6 2.4GHz receiver, BLDC motors, Electronic Speed Controllers (ESCs), and a power 
distribution board. 
 
**Detailed Working of the Drone System and Data Flow** 
The drone system operates based on real-time communication between the transmitter 
(controller) and the receiver onboard the drone. Commands given by the pilot are 
processed through a structured data flow, enabling precise control over the drone’s 
movement.  
How Commands Are Recognized and Processed 
**1. User Input (Transmitter Side)** 
• The pilot moves the control sticks on the FLYSKY FS-i6 transmitter to issue 
movement commands. 
• The transmitter converts the stick positions into PPM/PWM signals and encodes 
them for transmission. 
• A 2.4GHz RF signal is sent wirelessly from the transmitter to the drone’s receiver.

**2. Signal Reception (Drone Receiver Side)** 
• The FLYSKY FS-iA6B receiver on the drone receives the 2.4GHz RF signal. 
• It decodes the PPM/PWM signals and forwards them to the KK2.1.5 flight 
controller through individual channel outputs.

**3. Flight Controller Processing** 
• The KK2.1.5 flight controller processes the received signals, analyzing the 
required movement based on user input. 
• The gyroscope and accelerometer measure real-time orientation and flight 
conditions. 
• The flight controller calculates the necessary PWM adjustments for each motor to 
execute the desired motion. 
• Corrective actions are applied in real time to maintain stability and control.
 
**4. Signal Transmission to ESCs** 
• The KK2.1.5 sends specific PWM signals to the Electronic Speed Controllers 
(ESCs). 
• The ESCs regulate the power delivered to each BLDC motor, adjusting their speed 
accordingly.

**5. Execution of Drone Movement** 
• The BLDC motors respond by spinning at varying speeds, generating the required 
thrust and directional control. 
• The drone moves according to the pilot’s commands:  
o Throttle Up → Drone Ascends 
o Throttle Down → Drone Descends 
o Roll Left/Right → Drone Tilts Left/Right 
o Pitch Forward/Backward → Drone Moves Forward/Backward 
o Yaw Left/Right → Drone Rotates Left/Right

**6. Continuous Feedback and Adjustment** 
• The flight controller continuously monitors stability using its onboard 
gyroscope and accelerometer. 
• If external disturbances affect flight, the controller compensates by adjusting 
motor speeds automatically. 
• This ensures a smooth, stable, and responsive flying experience.

##  System Analysis of the Drone 📊📋
• **Communication:** The RF system enables bidirectional communication between the 
drone and the controller. Commands like flight direction, speed, altitude, and 
camera operation are sent via RF signals. 

• **Control Range:** RF systems determine the maximum distance at which the drone 
can be controlled. This range varies based on the power of the RF system and 
environmental conditions. 

• **Real-time Feedback:** RF systems provide real-time feedback from the drone to the 
operator, including video feed, telemetry data, and battery status.  

• **Complexity of Operation:** Operating RF drone systems may require technical 
expertise, especially in understanding frequency management, signal propagation, 
and troubleshooting interference issues. 

• **Susceptibility to Environmental Factors:** Environmental conditions such as rain, 
fog, and wind can affect RF signal strength and stability, potentially disrupting drone 
operations. 
