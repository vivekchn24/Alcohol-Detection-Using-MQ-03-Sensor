# 🚗 Alcohol Detection Using MQ-3 Sensor – IoT Mini Project (GTU Sem 7)

This repository contains a **mini project for the IoT (Internet of Things)** subject in **Semester 7** of **Gujarat Technological University (GTU)**. The project uses an **MQ-3 Gas Sensor** to detect alcohol presence and displays both analog and digital sensor values using an **Arduino board**.

--->>

## 📘 Subject: Internet of Things (IoT)  
## 🎓 University: Gujarat Technological University (GTU)  
## 👨‍💻 Project Type: Mini Project  
## 🧪 Component Used: MQ-3 Alcohol Detection Sensor  
## ⚙️ Platform: Arduino UNO

--->>

## 🛠️ Hardware Components

- Arduino UNO board
- MQ-3 Alcohol/Gas Sensor
- Breadboard and jumper wires
- USB cable for Arduino
- Power supply (via USB)

--->>

## 💡 Project Objective

To create a low-cost **alcohol detection system** using the MQ-3 gas sensor which can output both **digital and analog** readings based on the presence of alcohol in the environment.

--->>

## 📟 Code Explanation

```cpp
int digitalsensor = 2;
int analogsensor = A0;

void setup()
{
    pinMode(digitalsensor, INPUT);
    Serial.begin(9600);
}

void loop()
{
    bool digital = digitalRead(digitalsensor);
    int analog = analogRead(analogsensor);
    
    Serial.print("Analog value = ");
    Serial.print(analog);
    Serial.print("\t");
    Serial.print("Digital Value = ");
    Serial.print(digital);
    Serial.print("\n");
    
    delay(1000);
}

## 🔍 Functionality
- Reads analog value from the MQ-3 sensor via pin A0
- Reads digital value from pin 2
- Displays both values on the Serial Monitor
- Updates every 1 second (delay(1000))

## 🧪 How It Works
- When alcohol is detected in the air, the analog value increases.
- The digital output changes based on a pre-set threshold in the sensor module.
- This basic detection method can be used for breathalyzer prototypes or vehicle driver safety systems.

## 📌 Note
- This is a basic prototype for educational purposes only.
- Accuracy depends on proper calibration and environment conditions.
