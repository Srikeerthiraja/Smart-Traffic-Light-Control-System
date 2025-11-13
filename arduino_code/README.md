# Arduino Control Module 

###  Overview
This module manages the physical traffic signal lights (Red, Yellow, Green) based on the timing decisions received from the Python controller.  
It uses **Arduino Uno** to control LEDs connected to digital pins representing the signals.

---

###  Communication
- Receives signal duration and sequence via **serial communication** from the Python program.  
- Example data format: `{"green": 15, "yellow": 3, "red": 10}`  
- Arduino interprets this and switches LEDs accordingly.

---

###  Hardware Setup
| Component | Description |
|------------|-------------|
| Arduino Uno | Main microcontroller |
| LEDs | Represent traffic lights |
| Resistors | 220Ω for each LED |
| USB Cable | Communication and power |

---

###  Example (Pseudocode)
```cpp
int red = 13;
int yellow = 12;
int green = 11;

void setup() {
  Serial.begin(9600);
  pinMode(red, OUTPUT);
  pinMode(yellow, OUTPUT);
  pinMode(green, OUTPUT);
}

void loop() {
  if (Serial.available() > 0) {
    String data = Serial.readStringUntil('\n');
    int g = 15; // Placeholder for parsed value
    int y = 3;
    int r = 10;

    digitalWrite(green, HIGH);
    delay(g * 1000);
    digitalWrite(green, LOW);

    digitalWrite(yellow, HIGH);
    delay(y * 1000);
    digitalWrite(yellow, LOW);

    digitalWrite(red, HIGH);
    delay(r * 1000);
    digitalWrite(red, LOW);
  }
}
