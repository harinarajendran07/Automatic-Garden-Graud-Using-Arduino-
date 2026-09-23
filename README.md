# **AUTOMATIC GARDEN GUARD USING ARDUINO**

## Aim

To design and implement an Arduino-based smart garden guard system that detects an intruder (bird/animal) approaching the garden using an ultrasonic sensor, and automatically alerts with a buzzer and LED while moving a servo motor to scare it away.

# Components Required

1. Arduino Uno board  
2. HC-SR04 Ultrasonic Distance Sensor  
3. SG90 Micro Servo Motor  
4. Buzzer  
5. LED (with 220Ω resistor)  
6. Breadboard  
7. Jumper wires (male-male, male-female)  
8. USB cable (Arduino to PC)  
9. Cardboard box (model garden enclosure)  
10. Craft materials (paper plant, colored sticks — for the model display only)

# Procedure

1. Mount the HC-SR04 sensor at the entrance of the model garden, facing outward to detect approaching objects.  
2. Connect HC-SR04: VCC → 5V, GND → GND, Trig → digital pin (e.g. D9), Echo → digital pin (e.g. D10).  
3. Connect the buzzer's positive terminal to a digital pin (e.g. D7) through the breadboard, and ground to GND.  
4. Connect the LED anode (through resistor) to a digital pin (e.g. D6), cathode to GND.  
5. Connect the servo: signal wire to a PWM pin (e.g. D5), power to 5V, ground to GND.  
6. Connect the Arduino to the PC via USB and open the Arduino IDE.

# Working

The HC-SR04 sensor continuously sends ultrasonic pulses and measures the time taken for the echo to return, which the Arduino converts into distance. When an object (representing a bird or animal) comes within the set threshold distance, the Arduino triggers the buzzer to produce sound, turns on the LED as a visual alert, and rotates the servo motor to simulate a scaring motion (like a moving arm or flag). Once the object moves away, the system returns to its idle/monitoring state.

&nbsp;

&nbsp;

## Observation

1. The buzzer and LED activate only when an object is within the threshold distance, confirming accurate detection by the ultrasonic sensor.  
2. The servo motor responds correctly by rotating each time an intrusion is detected.  
3. The system resets automatically once the object leaves the detection range, showing reliable real-time monitoring.  
4. Detection accuracy may vary slightly with soft or angled surfaces due to ultrasonic reflection properties.

&nbsp;