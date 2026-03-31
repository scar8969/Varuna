# Varuna Autonomous Underwater Submarine System
Autonomous underwater robotic system using Raspberry Pi, Pixhawk  BlueOS with real- time video transmission via Ethernet


VARUNA is a custom-designed modular underwater drone (ROV) built for deep-sea exploration, inspection, and research applications. It integrates mechanical design, embedded systems, and AI-driven software to create a robust and adaptable underwater platform.

Designed with a focus on modularity, resilience, and scientific adaptability, VARUNA serves as a floating research lab capable of real-time sensing, navigation, and intelligent decision-making.

🎯 Key Features
⚙️ 5-Thruster Configuration for full 6 DOF motion
🧠 Onboard Intelligence (Computer Vision + SLAM ready)
🔋 High Endurance Power System (Multi LiPo setup)
🌊 Pressure-Resistant Hull (Up to ~85m depth)
⚖️ Neutral Buoyancy & Passive Stability
🔌 Hybrid Control System (Raspberry Pi + Pixhawk + MCU)
📡 Flexible Communication (Tethered + Acoustic-ready)
🧩 Modular Architecture for easy upgrades


🛠️ System Architecture
                +----------------------+
                |   Raspberry Pi 5     |
                | (High-Level Control) |
                +----------+-----------+
                           |
        +------------------+------------------+
        |                                     |
+---------------+                    +----------------+
|  Pixhawk / MCU |                  |   Sensors       |
| (Low-Level Ctrl)|                 | IMU, Depth, Cam |
+-------+--------+                  +--------+-------+
        |                                     |
        +-------------+-----------------------+
                      |
               +------+------+
               |   ESCs      |
               +------+------+
                      |
               +------+------+
               | Thrusters x5|
               +-------------+

               
⚙️ Technical Specifications
Parameter	Value
Max Depth	85 meters
Speed	2.5 m/s
Endurance	~2 hours
Weight	4–7 kg
Power	4S LiPo (5200mAh × multiple)
Thrusters	5 (BLDC-based)
Compute	Raspberry Pi 5 + Pixhawk + Teensy
Sensors	IMU, Depth, Temperature, Camera

<img width="554" height="94" alt="image" src="https://github.com/user-attachments/assets/b8459a72-820f-47f6-82e5-d43baa8752b2" />


🔩 Propulsion System
5 Thrusters:
2 Horizontal → Surge & Yaw
3 Vertical → Heave, Pitch & Roll

🧱 Mechanical Design
🧩 3D Printed Polymer Hull
🔍 Transparent Acrylic Electronics Bay
🔒 Multi O-ring sealing system
🧲 Adjustable ballast for buoyancy


Stability Principle:
Center of Buoyancy (CB) > Center of Gravity (CG) → Passive stability
🔌 Electronics & Power
⚡ Separate power rails (Logic & Motors)
🔄 MOSFET + Relay-based control
🔇 EMI mitigation using shielding & twisted pairs


Core Components:
Raspberry Pi 5
Pixhawk Flight Controller
ESCs (4-in-1 + individual)
Depth Sensor (MS5837)
IMU
Camera (Sony IMX series)

📡 Communication
Internal:
UART
I2C
SPI
External:
🔗 Tethered Ethernet (Testing & Control)
🌊 Acoustic Communication (Future Scope)
💡 Optical Communication (Short-range high-speed)
🤖 Software Stack
🐧 Linux-based system (Raspberry Pi)
🐍 Python for high-level control
🤖 SLAM & Computer Vision ready
🎯 Sensor Fusion (IMU + Depth)
⚙️ Low-level firmware on MCU


📦 Project Structure
VARUNA/
│
├── hardware/
│   ├── CAD/
│   ├── PCB/
│   └── mechanical/
│
├── software/
│   ├── control/
│   ├── vision/
│   └── communication/
│
├── docs/
│   ├── technical_report.pdf
│   ├── design_sheets/
│   └── diagrams/
│
├── simulations/
│
└── README.md

🧪 Applications
🌊 Marine Research & Surveys
🏗️ Underwater Infrastructure Inspection
🏺 Archaeological Exploration
🌱 Environmental Monitoring
🔍 Search & Rescue Operations
🔮 Future Work
Autonomous navigation (full AUV mode)
Advanced SLAM implementation
Acoustic communication integration
AI-based object detection & classification
Swarm robotics (multi-drone coordination)
