# Smart-Traffic-Light-Control-System
### Overview
The Smart Traffic Light Control System is an intelligent traffic management solution designed to minimize waiting times and reduce congestion at intersections.  
Using **computer vision (OpenCV)** and **Arduino**, the system detects real-time vehicle density and dynamically adjusts signal durations based on traffic flow.

This project was developed as part of a 6-member team to explore the application of AI and embedded systems in smart city development.

---

### Problem Statement
Conventional traffic lights operate on fixed intervals, which often leads to inefficiency — long waiting times during low traffic and congestion during peak hours.  
This project aims to **make traffic control adaptive** by analyzing real-time camera feeds to determine vehicle counts and adjusting signal durations accordingly.

---

###  Key Features
- Real-time vehicle detection using **OpenCV-Python**.  
- Dynamic signal timing adjustment using **a custom control algorithm**.  
- **Arduino microcontroller** used to manage LED-based traffic signals.  
- Achieved a **23% reduction in average vehicle waiting time** during testing.  
- Modular code structure for easy updates and scalability.

---

###  System Architecture
1. **Camera Module** → Captures live traffic feed.  
2. **Vehicle Detection Module (Python + OpenCV)** → Counts vehicles using contour detection.  
3. **Control Logic (Python)** → Calculates optimal green signal duration.  
4. **Arduino Module** → Receives updated timing via serial communication and controls the lights.  

---

###  Tech Stack
- **Programming Languages:** Python, C++ (Arduino)  
- **Libraries:** OpenCV, NumPy  
- **Hardware:** Arduino Uno, LEDs, USB Camera  
- **Tools:** Serial Communication, Python IDE  

---

###  Team and Contributions
**Team Size:** 6 Members  
**My Role:** Algorithm Design, Integration & Testing  

- Designed the signal-switching algorithm to adjust light durations dynamically.  
- Integrated real-time vehicle detection with Arduino signal control.  
- Conducted testing and documented results on performance improvement.  

---

###  Results
- Reduced average waiting time by **23%** compared to static timing models.  
- Improved **signal efficiency** and **reduced idle time** at low-traffic junctions.  

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

###  Author
**Keerthi Raja**  
B.Tech – Computer Science and Engineering  
[LinkedIn](#) | [GitHub](#) | [Email](mailto:srikeera@gmail.com)
