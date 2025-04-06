# ✈ ▷ Flight Controller (KK2.1.5):
You can check the complete instruction manual of KK2.1.5 Flight Controller (Credits: https://dl.btc.pl/kamami_wa/hk_54299_7.pdf) with this link.   

*Stabilization and balancing* of the UAV is done by the flight controller. It continuously takes measurements from the sensors (IMU, barometer etc.) and makes the required adjustments to the speed of the 
rotors through the ESC to keep the body stable and carry out the required movement (pitch, yaw, roll). The flying capabilities consist of the following factors:

*Gyro stabilization:* The ability to keep the UAV stable and level.

*Self-leveling:* The ability to automatically adjust itself during any orientation so the UAV stays level.

*Altitude Hold:* The ability to hover at a certain altitude over the ground.

The KK2.1.5 was engineered from the ground up to bring multi-rotor flight to everyone, not just the experts. The LCD screen and built-in software makes install and setup easier than ever.
A host of multi-rotor craft types are pre-installed, simply select your craft type, check motor layout/propeller direction, calibrate your ESCs and radio and your are ready to go! All of which is done with
easy-to-follow on-screen prompts!

- The original KK gyro system has been updated to an incredibly sensitive 6050 MPU system making this the most stable KK board ever and allowing for the addition of an auto-level function. 

- At the heart of the KK2.1.5 is an Atmel Mega644PA 8-bit AVR RISC-based microcontroller with 64k of memory. An additional header has been added for voltage detection, so no need for on-board soldering.

- A handy piezo buzzer is also included with the board for audio warning when activating and deactivating the board.

- Its operating voltage is 1.8V to 5.5V and its input voltage is 4.8-6.0 V.

 ---
## ✈️ *Flight Controller Specifications:*

| **Specification**             | **Details**                          |
|-------------------------------|--------------------------------------|
| **Size**                      | 50.5mm × 50.5mm × 12mm               |
| **Weight**                    | 21g (including Piezo buzzer)         |
| **Microcontroller (IC)**      | ATmega644PA                          |
| **Gyro/Accelerometer**        | MPU6050 (InvenSense Inc.)            |
| **Auto-level Support**        | Yes                                  |
| **Input Voltage Range**       | 4.8V – 6.0V                          |
| **AVR Interface**             | Standard 6-pin                       |
| **Receiver Signal**           | 1520 µs (5 channels)                 |
| **ESC Signal Output**         | 1520 µs                              |
| **Firmware Version**          | V1.17S1                              |
| **Pre-installed Firmware**    | Yes                                  |
| **Supported Copter Modes**    | Dualcopter                           |

---



## ✈️ *Flight Controller Setup: KK2.1.5*

Setting up the KK2.1.5 board is an essential process before flying your quadcopter. Follow these steps carefully to ensure everything is calibrated and configured properly.


### 🔌 Step 0: Initial Setup  
- **Ensure Transmitter is ON**
- **Bind Receiver to Transmitter**
- **KK2.1.5 Buttons**:  
  Use the four buttons on the board: **S1, S2, S3, S4** to navigate the onboard menu.

---

### ⚙️ Step 1: Load Motor Layout  
- Press **S4** to enter the **Menu**.  
- Go to **“Load Motor Layout”**.  
- Select **“Quadcopter X-Mode”** and configure your setup accordingly.  
- ✅ **Check all motor directions** to match the layout.

---

### 📏 Step 2: ACC (Accelerometer) Calibration  
- Place the quadcopter on a flat, level surface.  
- Navigate to **“ACC Calibration”** in the menu.  
- Press **S4** to start the **Auto Calibration**.  
- Once done, **remove and reconnect power**.  
- If LCD shows **“SAFE”**, calibration is successful ✅.

---

### 🔧 Step 3: PI Editor Configuration  
- Navigate to **PI Editor**.  
- Adjust **P Gain / Limit** and **I Gain / Limit** for:
  - **Aileron (Roll)**
  - **Elevator (Pitch)**
  - **Rudder (Yaw)**

#### 📌 Notes:
- **P Gain** = Proportional Gain → Controls **sensitivity & response**
  - Higher P = Sharper control
  - Lower P = Smoother control
- **I Gain** = Integral Gain → Controls **altitude holding**

---

### 🔄 Step 4: Mode Settings  
- Go to **Mode Settings**.  
- Set **“Self-Level” to AUX** (for automatic leveling during flight).

---

### ⚡ Step 5: Miscellaneous Settings  
Set **Voltage Alarm** for battery monitoring.

#### 📐 Alarm Voltage Calculation:
- For a **3-cell (3S) LiPo battery (11.1V)**  
  - Minimum safe voltage = 3.6V per cell  
  - Alarm setting = 3.6 × 3 × 10 = **108**

✅ Set **Alarm Level = 108** in **1/10 Volts**

---

### 🔁 Step 6: ESC Calibration  
- Turn on transmitter and **set throttle to minimum**  
- Then move **throttle to maximum**
- Hold **S1 + S4** and **connect battery**  
- Wait for **2 beeps**, then move **throttle down**  
- A final **1 beep** confirms calibration is complete ✅

---

### 🕹️ Step 7: Arming the Quadcopter  
- To arm: **Move throttle stick (left-hand side) down & to the right**
- Once armed, the quadcopter is ready for flight! 🛫


