# Smart-Traffic-Light-Control-System
### Overview
The Smart Traffic Light Control System is an intelligent traffic management solution designed to minimize waiting times and reduce congestion at intersections.  
Using **computer vision (OpenCV)** and **Arduino**, the system detects real-time vehicle density and dynamically adjusts signal durations based on traffic flow.

This project was developed as part of a 6-member team to explore the application of AI and embedded systems in smart city development.

## Problem Statement
Conventional traffic lights operate on fixed timing cycles regardless of traffic conditions.
This leads to inefficiency:
- Long waiting times at low-traffic periods
- Congestion during peak hours
- Increased fuel consumption and pollution

Goal: Create a system that **adapts traffic signals dynamically** based on real-time traffic data to reduce waiting times and improve intersection efficiency.

## Solution Overview
This project implements a **Smart Traffic Light Control System** using **computer vision (OpenCV)** and **Arduino**:

- **Real-time vehicle detection** using camera feeds and contour analysis in Python
- **Dynamic signal timing** with a custom algorithm that calculates green-light durations based on vehicle density
- **Arduino-controlled LEDs** to simulate real traffic lights
- **Integration and testing** to measure improvement in traffic flow

The system reduced **average waiting time by 23%** during testing, demonstrating the effectiveness of adaptive traffic management.


###  Key Features
- Real-time vehicle detection using **OpenCV-Python**.  
- Dynamic signal timing adjustment using **a custom control algorithm**.  
- **Arduino microcontroller** used to manage LED-based traffic signals.  
- Achieved a **23% reduction in average vehicle waiting time** during testing.  
- Modular code structure for easy updates and scalability.

---
###  Tech Stack
- **Programming Languages:** Python, C++ (Arduino)  
- **Libraries:** OpenCV, NumPy  
- **Hardware:** Arduino Uno, LEDs, USB Camera  
- **Tools:** Serial Communication, Python IDE  
 

---

###  System Architecture
1. **Camera Module** → Captures live traffic feed.  
2. **Vehicle Detection Module (Python + OpenCV)** → Counts vehicles using contour detection.  
3. **Control Logic (Python)** → Calculates optimal green signal duration.  
4. **Arduino Module** → Receives updated timing via serial communication and controls the lights. 


---

## Design Decisions & Trade-offs

### Real-Time Vehicle Detection vs Sensor-Based Detection
- **Choice:** Computer vision using OpenCV
- **Gain:** Low-cost, non-intrusive, flexible for multiple lanes
- **Trade-off:** Sensitive to lighting/weather conditions; may require calibration

### Dynamic Signal Algorithm vs Fixed-Timing
- **Choice:** Adaptive timing based on vehicle counts
- **Gain:** Reduced waiting time and congestion
- **Trade-off:** Slightly more complex control logic; requires robust testing to prevent errors

### Arduino + Python Integration vs Full Embedded System
- **Choice:** Arduino handles hardware control, Python handles detection & algorithm
- **Gain:** Easy to prototype and test; modular
- **Trade-off:** Slight latency due to serial communication; not a production-ready embedded solution

### Multi-Lane / City-Wide Coordination
- **Choice:** Only single intersection implemented
- **Trade-off:** City-wide optimization would need IoT integration and more complex coordination
---

## Results
Performance was evaluated by comparing the adaptive system to a fixed-timing traffic light:

| Metric                     | Fixed Timing | Adaptive System | Improvement |
|-----------------------------|-------------|----------------|------------|
| Average Vehicle Waiting Time | 60 seconds  | 46 seconds     | 23%        |
| Signal Idle Time             | High        | Reduced        | yes         |
| Traffic Flow Efficiency      | Low         | Improved       | yes          |

The reduction in waiting time indicates the system can **respond effectively to real-time traffic conditions**.


---

###  Future Enhancements
- Integrate IoT-based sensors for more accurate traffic measurement.  
- Create a dashboard for real-time monitoring and data analytics.  
- Implement a city-wide coordination mechanism between intersections.  

---

###  License
This project is for educational and demonstration purposes only.  
Developed as part of an academic initiative under the **Vellore Institute of Technology, Andhra Pradesh**.

---

###  Team and Contributions
**Team Size:** 6 Members  
**My Role:** Algorithm Design, Integration & Testing  

- Designed the signal-switching algorithm to adjust light durations dynamically.  
- Integrated real-time vehicle detection with Arduino signal control.  
- Conducted testing and documented results on performance improvement. 
