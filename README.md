# Line-Following-Robot
Line Following Robot 🚗
This repository contains the implementation of a Line Following Robot using Aseba language and Thonny IDE. The robot is designed to detect and follow a line, while dynamically responding to obstacles using proximity sensors and motor control.

🛠 Features
Line Following Algorithm: Based on proportional (P) or proportional-integral (PI) control.
Proximity Sensor Integration: Detects objects using multiple proximity sensors for better accuracy.
Motor Control: Smooth forward, backward, and turning motions using real-time feedback.
State Machine Logic: Efficiently manages robot states like line following, obstacle detection, and recovery.
🔧 Hardware Components
Proximity Sensors:
prox.horizontal[0] to prox.horizontal[4]: Used to detect lines and obstacles.
Motors:
Left and right motors controlled using target values.
Power Supply:
Rechargeable batteries for powering the robot.
Controller:
Thymio robot or any Aseba-compatible device.
📂 Repository Structure

line-following-robot/
│
├── aseba/
│   ├── line_following.aesl       # Aseba script for line following
│   ├── bang_bang_control.aesl    # Aseba script for bang-bang control
│   ├── pi_control.aesl           # Aseba script for PI control
│
├── thonny/
│   ├── main.py                   # Python script for motor and sensor integration
│   ├── sensor_test.py            # Script for testing proximity sensors
│
├── docs/
│   ├── state_diagram.pdf         # State diagram for the robot's logic
│   ├── setup_guide.md            # Step-by-step guide to set up the project
│   ├── troubleshooting.md        # Common issues and fixes
│
├── media/
│   ├── robot_demo.mp4            # Video demonstration of the robot
│   ├── line_following_plot.png   # Plot of error vs. distance
│
└── README.md                     # Project overview (this file)
🖥 Software Setup
Aseba Language
Download and install Aseba Studio.
Aseba Download Link
Load the scripts from the aseba/ folder:
line_following.aesl for basic line following.
pi_control.aesl for proportional-integral control.
Thonny IDE
Install Thonny IDE.
[Thonny Download Link](https://mobsya.github.io/aseba/index.html)

🧠 How It Works
Key Algorithms
Bang-Bang Control:

Compares the reference value with the sensor reading and adjusts the motor targets abruptly (e.g., full speed forward or full stop).
Simple and fast but less precise.
Proportional-Integral (PI) Control:

Adjusts motor power based on the error (difference between reference and measured values) and the accumulated error over time.
Offers smoother and more precise control.
State Machine Logic:

State 1: Line following.
State 2: Obstacle detection.
State 3: Recovery behavior when off-path.
🧪 Observations
Bang-Bang Control:

The robot stops abruptly near objects and reverses.
Effective for simple tasks but results in jerky motion.
PI Control:

The robot smoothly slows down as it approaches obstacles and stops accurately.
Achieves better error management and smoother navigation.
State Machine:

Handles multiple scenarios effectively by transitioning between states like line following, obstacle detection, and recovery.
📊 Results
Plots:
Plots show the robot’s error and speed variations during line following.
PI control has less error variance compared to Bang-Bang control.
🚀 Future Improvements
Add PID Control: Enhance control by integrating a derivative term for smoother transitions.
Computer Vision: Use a camera for advanced line detection and navigation.
IoT Integration: Monitor and control the robot remotely using IoT.
Obstacle Avoidance: Combine line following with dynamic obstacle avoidance using additional sensors.


