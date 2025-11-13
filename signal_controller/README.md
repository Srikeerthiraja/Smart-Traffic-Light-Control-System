# Signal Controller Module 

###  Overview
This module serves as the **core decision-making system** of the Smart Traffic Light Control project.  
It receives real-time vehicle count data from the **Vehicle Detection Module**, processes it using a custom algorithm, and dynamically determines the duration of each traffic light.  
The calculated signal timings are then transmitted to the **Arduino Control Module** for execution.

---

###  Workflow
1. **Input:** Vehicle count from the detection module (via file, API, or serial input).  
2. **Processing:** Applies a dynamic timing algorithm to decide green, yellow, and red durations.  
3. **Output:** Sends timing instructions to Arduino using serial communication.  
4. **Feedback Loop:** Continuously updates based on real-time vehicle data every few seconds.

---

###  Algorithm 
```python
def calculate_signal_times(vehicle_count):
    # Minimum and maximum durations in seconds
    min_green = 10
    max_green = 40
    threshold = 15  # vehicles

    # Dynamic allocation based on vehicle density
    if vehicle_count < threshold:
        green_time = min_green
    else:
        green_time = min(max_green, min_green + (vehicle_count - threshold) * 2)

    yellow_time = 3
    red_time = 10
    return {"green": green_time, "yellow": yellow_time, "red": red_time}
