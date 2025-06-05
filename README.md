# 🛣️ Autonomous Vehicle Navigation in CARLA Simulator

This project implements a comprehensive autonomous driving pipeline in the [CARLA Simulator](https://carla.org/) for waypoint tracking and stop sign compliance, utilising computer vision, LiDAR, and PID controllers. Designed for simulation-based validation of planning, perception, and control systems.

## 🚗 Project Overview

The ego vehicle navigates a set of waypoints and comes to a full stop at traffic signs in a simulated urban environment. The system achieves:

- **<0.15 m/s speed error**
- **<0.5 m lateral tracking error**
- **5000+ simulation frames** with **zero collisions**
- **Consistent stop sign compliance** within specified zones

## 🧠 Key Features

- **Perception**  
  - Traffic sign detection using **OpenCV**  
  - LiDAR-based obstacle mapping using **PCL**

- **Planning**  
  - Waypoint interpolation and velocity profiling  
  - Behavioral state transitions for navigation and stopping

- **Control**  
  - **PID controllers** for throttle, brake, and steering  
  - Smooth and responsive control behavior

- **Visualization**  
  - Real-time performance graphs using `matplotlib` and a custom **live_plotter**  
  - Telemetry logging for trajectory tracking and analysis

## 🛠️ Tools & Libraries

- **CARLA Simulator** (v0.9.x)
- **Python 3.6+**
- **OpenCV**, **PCL**, **NumPy**, **Matplotlib**
- Custom modules: `controller2d`, `local_planner`, `behavioral_planner`, `live_plotter`

## 📁 Project Structure

Course4FinalProject/
├── module_7.py             # Main entry point
├── controller2d.py         # PID controller
├── behavioral_planner.py   # FSM for decision making
├── local_planner.py        # Path interpolation & control point generation
├── live_plotter.py         # Real-time plotting interface
└── trajectory.txt          # Logged trajectory for evaluation


## 🚦 Evaluation Criteria

The vehicle was assessed based on:
- Accurate trajectory following  
- Full stop at the designated stop zone  
- Collision-free behavior

## ✅ Results

Successfully passed all evaluation checks, including:
- Complete stop within the target zone  
- No collisions  
- Clean waypoint navigation over all test episodes

## 📌 Setup Instructions

1. Install CARLA simulator (Windows x64 recommended)  
2. Clone this repository under `PythonClient/` in your CARLA folder  
3. Run using:
   ```bash
   py -3.6 module_7.py

## 🎥 Demo Video

📽️ [Watch the demo video](https://drive.google.com/file/d/1RsIK81WRpiSUAICjSKXhhmo2GXR44nZw/view?usp=sharing)
