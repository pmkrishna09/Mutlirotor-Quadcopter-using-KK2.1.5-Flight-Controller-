# MultiWii Open Source Software

You can check the MultiWii official website for MultiWii Software Parameters and Configuration (Credits: http://www.multiwii.com/software).

I used this flight simulation software because to check the ESCs and BLDC Motors can work using Arduino boards or not in precise. These ideas branches into another project where building drone using Arduino and 
STM32 as a Flight Controller.

- MultiWii is a general purpose software to control a multirotor RC model.
- It can now use various sensors but wasÂ initiallyÂ developedÂ to support Nintendo Wii console gyroscopes and accelerometers.
- We can find these sensors in the extensions of the Nintendo WiiMote: Wii Motion Plus and Wii Nunchuk.

This project was an opportunity to develop my own software on an Arduino platform.
- The achieved stability is excellent for FPV and allows any kind of acrobatics.
- The software is for the moment able to control Â a tricopter, a quadricopter or a hexacopter.

---

## MultiWii GUI Parameter Configuration
MultiWii GUI Parameter Configuration

let's get to know the meaning of each area in GUI, as shown
Here’s a well-structured, clear, and user-friendly walkthrough of the **MultiWii GUI Overview and Configuration Steps**, including **meaning of GUI areas**, **calibration**, **PID/throttle setup**, and **flight mode configuration**, using tables and headings for clarity.

---

## 🧭 MultiWii GUI Overview

Let's get familiar with each section of the MultiWii Graphical User Interface (GUI):

| 🧩 **GUI Area**                          | 📋 **Description**                                                                 |
|----------------------------------------|----------------------------------------------------------------------------------|
| **Serial Port Selection**              | Selects the COM port to which your flight controller is connected.               |
| **Throttle Curve Setting**             | Adjusts throttle sensitivity and smoothness.                                     |
| **Remote Control Curve Setting**       | Fine-tunes the response of the remote control sticks.                            |
| **PID Parameters Adjustment**          | Used to adjust flight behavior and stability.                                    |
| **Flight Mode Setting**                | Allows configuration of different flight modes (e.g., ANGLE, HORIZON, MAG, etc.) |
| **Output Channels for Remote Control** | Displays channels received from the transmitter.                                 |
| **Motor Output**                       | Shows real-time PWM output sent to ESCs.                                         |
| **Attitude Angles**                    | Displays pitch, roll, and yaw angles.                                            |
| **Activation State for Sensors**       | Shows which sensors (e.g., MAG, BARO) are currently active.                      |
| **Read Parameters**                    | Reads saved configuration parameters from the flight controller.                 |
| **Reset Parameters**                   | Resets the configuration to default values.                                      |
| **Calibrate Magnetometer**            | Starts the magnetometer (compass) calibration routine.                           |
| **Calibrate Accelerometer**            | Starts the accelerometer calibration process.                                    |
| **Write Parameters**                   | Saves all modified parameters to the flight controller.                          |
| **Start/Stop Sensor Data Output**      | Toggles the sensor data output to the GUI.                                       |
| **Sensor Data**                        | Displays real-time data from accelerometer, gyroscope, barometer, etc.          |
| **Output Curve of Sensors**            | Shows graphical curves of sensor outputs.                                        |
| **3D Diagram for Quadcopter**          | Provides a 3D visual representation of quadcopter orientation.                   |
| **Direction Angle**                    | Displays the directional (heading) angle.                                        |
| **GPS Output Data**                    | Shows data such as coordinates, satellite count, and fix status.                 |

---

## 🧪 Calibration Procedures

### ⚖️ Calibrating Accelerometer

1. Place the quadcopter on a **level surface**.
2. Connect to your PC via **FTDI**.
3. Open **MultiWii GUI** and click on **`CALIB_ACC`**.
4. The ACC values should update to approximately:
   - **Pitch: 0**
   - **Roll: 0**
   - **Z-axis: 512**
5. ✅ Calibration complete!

---

### 🧭 Calibrating Magnetometer

1. After ACC calibration, click **`CALIB_MAG`**.
2. The LED on the flight controller will start blinking.
3. **You have 30 seconds** to:
   - Rotate the flight controller **360°** on **all three axes** (Pitch, Roll, Yaw).
   - Complete **2 full spins per axis** for best results.
4. ✅ Test calibration using a digital compass for verification.

---

## ⚙️ PID Parameters Adjustment

| 🔧 **Parameter** | 📌 **Function**                                  |
|----------------|--------------------------------------------------|
| **P Gain**     | Controls **sensitivity and sharpness** of response |
| **I Gain**     | Affects **stability and level holding over time** |

- Hover over a PID parameter → **Hold left mouse button** → **Move mouse left/right** to adjust.
- Default values work well for beginners. Fine-tune only when necessary.

---

## 📈 Throttle Curve Adjustment

### 🛸 Why Adjust?
- Helps in **smooth throttle control**, especially for beginners.
- Prevents sudden jerks in altitude.

### 🛠️ Example Settings:
| ⚙️ **Curve** | 🔢 **Value** |
|-------------|--------------|
| **MID**     | 0.4          |
| **EXPO**    | 0.7          |

> 🔁 **Remote Control Curve**: Leave the default values unless fine-tuning is needed.

---

## ✈️ Flight Mode Configuration

| 🎮 **Flight Mode** | 🧩 **Function**                                      |
|-------------------|-----------------------------------------------------|
| **ARM**           | Lock/unlock the flight controller                   |
| **ANGLE**         | Self-stabilization (auto-leveling)                  |
| **HORIZON**       | Hybrid mode (manual + auto-level)                   |
| **BARO**          | Maintains altitude using barometric sensor          |
| **MAG**           | Maintains heading using magnetometer                |
| **HEADFREE**      | Headless mode – orientation-independent control     |
| **HEADADJ**       | Adjust head direction during flight                 |
| **GPS HOME**      | Returns to starting point (if GPS is enabled)       |
| **GPS HOLD**      | Hovers in place (fixed GPS position)                |

---

### 🎚️ Using AUX Switches for Mode Control

| **AUX Channel** | **Function**                                       |
|----------------|----------------------------------------------------|
| **AUX1 - AUX4** | Map flight modes to **3-stage switches**           |
| **LOW / MID / HIGH** | Correspond to **switch positions** on transmitter |

#### 🧠 Example Setup for AUX1:
| 🔄 **Switch Position** | 🎮 **Flight Mode Activated**                            |
|------------------------|--------------------------------------------------------|
| **LOW**                | ANGLE (Self-Stabilization)                             |
| **MID**                | ANGLE + HEADFREE (Headless Mode)                       |
| **HIGH**               | ANGLE + HEADFREE + BARO (Altitude Hold)                |

> ✔️ Click small **check marks** under AUX columns → White means "Active".  
> 🔐 Click **WRITE** to save changes.

---



*(Credits: http://wiki.sunfounder.cc/index.php?title=MultiWii_GUI_Parameter_Configuration)*

---


## MultiWii Wiki and Forum 
The Wiki is at: http://www.multiwii.com/wiki. Please note that the wiki no longer allows new sign-ups, probably due to spam.
The Forum is at: http://www.multiwii.com/forum/.
MultiWii Downloads
I decided to put these here because I have had trouble trying to find different versions of the software, so I thought it was worth putting them somewhere on the internet to make sure they stay available. 
These are also available on the Internet Archive.

Download link: https://e1.pcloud.link/publink/show?code=kZ1544ZifSuNqtybAL6c0N6TGH7HzJAmWik

Below is a list of what is available from the link.

MultiWii v2.4
MultiWii v2.3
MultiWii v2.2
MultiWii v2.1
MultiWii v2.0
MultiWii v1.9
MultiWii v1.8-patch2
MultiWii v1.8
MultiWii v1.7
LEDRin software (v2.0) and information
MultiWii connection diagrams.
MultiWii stick configuration diagrams.
An archive of the MultiWii source code respository.
*(Credits: https://www.hamishmb.com/multiwii-pages-and-downloads/)*

