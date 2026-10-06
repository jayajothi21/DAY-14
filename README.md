# DAY-14
AUTOMATRIX – Live Sensor + TinyML



# SIG-04 AUTOMATRIX – Live Sensor + TinyML

## Objective

Connect an LDR sensor to an ESP32 and use an on-device TinyML model to classify the light level as **Dark, Normal, or Bright**. The classification result is displayed on an OLED screen.

## System Workflow

```text
LDR Sensor
    ↓
ESP32
    ↓
LDR Analog Value
    ↓
TinyML Model
    ↓
Dark / Normal / Bright
    ↓
OLED Display
```

## Classes

The TinyML model classifies the light level into three categories:

* **Dark**
* **Normal**
* **Bright**

## Training Data

Synthetic LDR sensor values are used for model training.

| LDR Value   | Class  |
| ----------- | ------ |
| 0 – 1200    | Dark   |
| 1201 – 2800 | Normal |
| 2801 – 4095 | Bright |

## Sample Predictions

```text
LDR Value: 500  → Dark
LDR Value: 2000 → Normal
LDR Value: 3500 → Bright
```

## Technologies Used

* ESP32
* LDR Sensor
* OLED Display
* Google Colab
* Python
* TensorFlow
* TensorFlow Lite Micro
* TinyML

## Generated Files

* `SIG-04-Live-Sensor-TinyML.ipynb` – Google Colab notebook containing the training and TFLite conversion code.
* `light_model.tflite` – Converted TensorFlow Lite model.
* `light_model_data.h` – C/C++ header file used to embed the TinyML model in the ESP32 project.
* `README.md` – Project documentation.

## Result

The TinyML model is trained to classify LDR sensor readings into **Dark, Normal, and Bright** categories. The trained model is converted into TensorFlow Lite format and prepared for deployment on the ESP32. The predicted light level can be displayed on an OLED screen.

## Project Status

**TinyML model training and TFLite conversion completed.**

ESP32 live LDR sensing and OLED display are used for the final hardware implementation.
