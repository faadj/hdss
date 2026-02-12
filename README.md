# Hybrid Smart Detection System using yolo 11n  

**A Pervasive Computing Approach to Real-Time, On-Premises Fire and Smoke Detection**

## Project Overview
The Hybrid Smart Detection System (HSDS) is an advanced safety device designed to fix common problems found in standard fire alarms. Traditional sensors often trigger false alarms from cooking steam, while modern smart detectors rely too much on the cloud, which creates privacy risks and stops working if the internet goes down.

This project offers an on-site (edge computing) solution. It keeps all data private and works independently without needing a constant internet connection. By combining a chemical gas sensor with computer vision, the system can distinguish between harmless steam and actual fire hazards

## Key Features
* **Edge Computing & Privacy:** 
* **Context-Awareness:** 
* **Fully Autonomous:** 
* **Hybrid Logic:** 

<img width="714" height="342" alt="image" src="https://github.com/user-attachments/assets/903752c7-56eb-4ef0-b756-76b8a8ba2da4" />


## How It Works
The system uses a logic called "Sensor Fusion" to make decisions. It follows a three step process to ensure accuracy:
Monitoring: The device continuously checks air quality using a local sensor.
Trigger: If the gas sensor detects smoke (voltage exceeds THRS = V), it activates the camera for a 60-second scan.
Confirmation: logic analyzes the video feed. If it sees fire or smoke visually, it confirms the emergency and sends an alert.

<img width="644" height="325" alt="image" src="https://github.com/user-attachments/assets/40c2b40e-a7f1-4f3a-9618-97101faaabc3" />


## Hardware & Tech Stack
Is project ko **Phase 2 Hybrid Implementation** tak develop kiya gaya hai. Niche di gayi core technologies use ki gayi hain:

* **Processing Unit:** NVIDIA Jetson Nano (Linux-based OS).
* **Sensors:** MQ-2 Gas Sensor (via ADC1115 converter) & 2MP USB Camera.
* **Language:** Python 3.11.
* **AI Inference Engine:** Ultralytics **YOLO11n** (Custom trained model).
* **Computer Vision:** OpenCV (`cv2`) for video stream handling.
* **Remote Logging:** ThingSpeak API (for monitoring sensor data).


## Performance & Results
A custom AI model was trained on a dataset of over 3,050 images containing fire and smoke. The training took place on Google Colab using a T4 GPU.
Performance metrics include:
## Precision: Stabilized around 80%, ensuring a low rate of false alarms.
## Recall: Reached between 85% and 90%, meaning the system reliably detects actual fires.
## Loss Convergence: The training graphs showed a steady improvement in the model's ability to locate and classify fire

<img width="678" height="432" alt="image" src="https://github.com/user-attachments/assets/37b5fa12-61d8-4388-afb2-66fe732e5705" />

<img width="564" height="563" alt="image" src="https://github.com/user-attachments/assets/0bbc738e-c2d1-443d-b5fc-9b5d5f5ddef0" />

<img width="611" height="379" alt="image" src="https://github.com/user-attachments/assets/975a66b5-9f71-4f39-a7ff-206f20f774b8" />


## Issues
* ** Failed to get callmebot API key for whatsapp alert messaging
