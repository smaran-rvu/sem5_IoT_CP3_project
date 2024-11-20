# Ultrasonic Flow Meter Fault Diagnosis Using Deep Learning and TinyML

This project integrates IoT and edge computing to develop a fault diagnosis system for liquid ultrasonic flowmeters. It leverages deep learning for high diagnostic accuracy and TinyML for deployment on resource-constrained devices like the ESP32 microcontroller.

---

## **Table of Contents**
- [Project Overview](#project-overview)
- [Features](#features)
- [System Requirements](#system-requirements)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Results](#results)
- [License](#license)

---

## **Project Overview**
The project demonstrates real-time fault diagnosis for ultrasonic flowmeters using deep learning. It processes data from the Meter D dataset, trains a compact neural network, and deploys the trained model on an ESP32 microcontroller for real-time edge computing applications.

### Key Highlights:
1. **Dataset:** Meter D dataset with 44 features and 4 output categories (Healthy, Gas Injection, Installation Effects, Waxing).
2. **Model:** Sequential neural network with 1,402 trainable parameters.
3. **Edge Deployment:** TensorFlow Lite model deployed on ESP32 using the EloquentTinyML library.
4. **Performance:** Achieved 91.67% test accuracy with inference latency under 20ms on ESP32.

---

## **Features**
- Real-time fault classification for ultrasonic flowmeters.
- Lightweight neural network optimized for edge devices.
- Seamless integration of deep learning with IoT technologies.

---

## **System Requirements**

### **Hardware:**
- ESP32 microcontroller
- Laptop or desktop for development and deployment

### **Software:**
- **Python 3.8+**
  - TensorFlow 3.x
  - Keras 2.6.0
  - Pandas and NumPy
- **Arduino IDE** for ESP32 programming
- **EloquentTinyML** library for TensorFlow Lite integration

---

## **Setup Instructions**

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd <project_directory>
   ```

2. **Install Python Dependencies:**
   ```bash
   pip install tensorflow keras pandas numpy
   ```

3. **Train the Model:**
   - Preprocess the dataset by normalizing input features.
   - Train the model using the provided script:
     ```bash
     python train_model.py
     ```
   - Save the trained model as a `.tflite` file.

4. **Convert to Header File:**
   ```bash
   xxd -i model.tflite > model.h
   ```

5. **Deploy on ESP32:**
   - Open the Arduino IDE.
   - Load the `fault_diagnosis.ino` sketch.
   - Upload the header file (`model.h`) to the ESP32 environment.
   - Compile and upload the code to ESP32.

---

## **Usage**

1. Power on the ESP32 device and ensure it is connected to the necessary sensors.
2. Input normalized data through the ESP32.
3. View the fault diagnosis results on the serial monitor.

---

## **Results**
- **Model Accuracy:** 91.67% on test data.
- **Inference Latency:** Less than 20ms on ESP32.
- **Real-Time Classification:** Accurate prediction of flowmeter health states into one of four categories.

---

## **License**
This project is released under the MIT License. See the `LICENSE` file for more details.

---

### For additional details or troubleshooting, please refer to the project documentation or contact the developer:  
**Smaran Rangarajan Bharadwaj**  
**Email:** [smaranrb.btech22@rvu.edu.in](mailto:smaranrb.btech22@rvu.edu.in)