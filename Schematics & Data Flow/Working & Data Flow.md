# 🛸 Detailed Working of the Drone System and Data Flow

The drone system functions through **real-time communication** between the pilot's transmitter and the onboard components of the drone. Each command is **recognized, processed, and executed** through a well-defined path involving the **FLYSKY FS-i6 Transmitter**, **FS-iA6 Receiver**, **KK2.1.5 Flight Controller**, **ESCs**, and **BLDC Motors**.

---

## 🧠 How Commands Are Recognized and Processed

### 1️⃣ User Input via Transmitter (FLYSKY FS-i6) 🎮

- 👨‍✈️ The pilot moves the **control sticks/switches**.
- 📶 These inputs are converted into **PPM/PWM signals**.
- 🎛️ Control channels: **Roll**, **Pitch**, **Yaw**, **Throttle**, **Flight Mode**, **AUX Functions**.
- 📡 Signals are encoded into **2.4GHz RF signals** and transmitted.

---

### 2️⃣ Signal Reception at the Drone (FLYSKY FS-iA6B Receiver) 📥

- 📻 The **FS-iA6B receiver** picks up the **2.4GHz signal**.
- 🔄 Decodes the PPM/PWM signals.
- 🧩 Forwards them through **individual channel outputs** to the **KK2.1.5 Flight Controller**.

---

### 3️⃣ Flight Controller Processing (KK2.1.5) 🧠⚙️

- 🧮 Acts as the **central processor**.
- 🔍 Uses onboard **gyroscope** and **accelerometer** to measure:
  - Orientation (Tilt, Rotation)
  - External Forces (e.g., wind)
- 🧠 Applies **flight stabilization algorithms**.
- 🎯 Generates precise **PWM signals** to control the **ESCs**.

---

### 4️⃣ Motor Speed Control via ESCs 🔌⚡

- 🔄 ESCs receive PWM signals from the flight controller.
- ⚙️ They **regulate power** to the BLDC motors.
- 🔧 Adjust **voltage and current** to control motor speed (RPM).

---

### 5️⃣ Execution of Movement via BLDC Motors 🚁

| ✏️ **Command**            | 🔄 **Motor Reaction**                        | 🛸 **Drone Movement**           |
|--------------------------|---------------------------------------------|-------------------------------|
| **Throttle Up**          | All motors increase speed                   | Drone **Ascends** ⬆️          |
| **Throttle Down**        | All motors decrease speed                   | Drone **Descends** ⬇️         |
| **Roll Left/Right**      | One side motors speed up/down               | Drone **Tilts** ↔️            |
| **Pitch Forward/Backward**| Front/back motors adjust speed             | Drone **Moves Forward/Back** ↕️ |
| **Yaw Left/Right**       | Opposing motors spin differently            | Drone **Rotates** ⤴️ / ⤵️     |

---

### 6️⃣ Real-Time Feedback and Stabilization 🔁📐

- 📡 Gyroscope & accelerometer provide continuous data.
- 💨 Detects any disturbance (e.g., wind).
- 🎯 Controller sends **automatic corrective signals** to ESCs.
- ✅ Ensures **stable**, **smooth**, and **responsive** flight.

---

## 🗂️ Step-by-Step Data Flow in the Drone System

| 🔢 **Step** | ⚙️ **Process**                               | 📍 **Details**                                                                 |
|------------|-----------------------------------------------|--------------------------------------------------------------------------------|
| 1️⃣         | **User Input**                               | Control sticks on transmitter moved → PPM/PWM signals encoded → RF signal sent |
| 2️⃣         | **Signal Reception**                         | Receiver captures 2.4GHz signal → Decodes & sends signals to flight controller |
| 3️⃣         | **Flight Controller Processing**             | Interprets inputs + sensor data → Generates PWM outputs for ESCs               |
| 4️⃣         | **Signal to ESCs**                           | ESCs receive PWM signals → Regulate motor power                                |
| 5️⃣         | **Motor Execution**                          | BLDC motors spin → Drone performs motion based on control input                |
| 6️⃣         | **Feedback & Correction**                    | Sensors detect drift → Controller adjusts motor speeds in real time            |

---

### 🧩 Summary: Drone Brain in Action!

🧠 Transmitter Input → 📡 RF Signal → 📥 Receiver → 🧠 Flight Controller  
→ 🔌 ESCs → ⚙️ Motors → ✈️ Flight → 🔁 Sensor Feedback → 🧠 Correction

---

