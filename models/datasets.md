# Datasets for DriveWise Models

This document centralizes all datasets and resources for training and evaluating DriveWise AI models.

---

## 1. Traffic Sign Recognition (TSR)

### GTSRB (German Traffic Sign Recognition Benchmark)
- **Link:** https://benchmark.ini.rub.de/gtsrb_dataset.html
- **Purpose:** Detect and classify road signs and speed limit panels
- **Format:** Image dataset
- **Status:** Primary dataset for model

---

## 2. Driver Behavior Analysis

Datasets for analyzing driving behavior, detecting risky patterns, fatigue, distraction, etc.

### 2.1 Multi-Class Driver Behavior Image Dataset
- **Link:** https://data.mendeley.com/datasets/mzb4b6dff3/1
- **Name:** DriverSVT
- **Description:** Collects vehicle telemetry via smartphone (accelerometer, gyroscope, magnetometer) + speed + driver states (drowsiness, distraction, seatbelt, phone usage, etc.)
- **Size:** 600M+ samples, 633 drivers
- **Format:** CSV
- **Labels:** K-means clustering segmentation → "parking & start", "city", "highway" scenarios
- **License:** Zenodo
- **Use Case:** Analyze driving patterns, detect risky behaviors

### 2.2 UAH-DriveSet
- **Link:** https://robesafe.uah.es/
- **Description:** DriveSafe app on smartphone records GPS, accelerometer, and rear camera video
- **Labels:** "normal", "drowsy", "aggressive"
- **Includes:** GPS data, geolocation, speed
- **Use Case:** Driving style analysis, dangerous behavior detection, aggression/drowsiness study

### 2.3 POLIDriving Dataset
- **Link:** (refer to MDPI publication)
- **Description:** Public-access dataset for road safety analysis. Integrates GPS, OBD (vehicle), smartphone, weather, and driver health data
- **Labels:** Risky driving patterns, potential accidents
- **Attributes:** ~32 attributes from heterogeneous sources (GPS, vehicle, weather, etc.)
- **Use Case:** Risk modeling, multi-source telemetry analysis

---

## 3. Activity Recognition

Datasets for recognizing driving and other human activities via smartphone sensors.

### 3.1 A Public Domain Dataset for Real-Life Human Activity Recognition
- **Link:** https://data.mendeley.com/datasets/
- **Description:** Smartphone-based activity recognition via GPS + accelerometer + gyroscope + magnetometer
- **Labels:** "inactive", "active", "walking", "driving"
- **GPS Variables:** latitude, longitude, altitude, bearing, speed, accuracy
- **Note:** GPS sampling frequency is not fixed (depends on Android device)
- **Use Case:** Activity classification, driving context detection

### 3.2 Smartphone Sensor Dataset for Driver Behavior Analysis
- **Link:** PubMed (article reference)
- **Description:** Smartphone sensors (accelerometer, gyroscope, GPS) for driver behavior classification
- **Format:** ML-ready for behavior classification
- **Use Case:** ML model training for driving behavior classification
---

## Summary Table

**Note:** This table lists datasets currently under research and evaluation. We are still in the research phase — no model implementation or integration has started yet. These datasets are potential candidates for future development.

| Model | Dataset | Size | Format | Status |
|-------|---------|------|--------|--------|
| Traffic Sign Recognition | GTSRB | N/A | Images | 📚 Research |
| Driver Behavior | DriverSVT | 600M+ samples | CSV | 📚 Research |
| Driver Behavior | UAH-DriveSet | Multi-source | Video + Sensors | 📚 Research |
| Driver Behavior | POLIDriving | N/A | Multi-source | 📚 Research |
| Activity Recognition | Public Domain Activity | N/A | Sensors + GPS | 📚 Research |
| Activity Recognition | Smartphone Behavior | N/A | Sensors + GPS | 📚 Research |

---

**Last Updated:** 2025-11-16  
**Status:** Preliminary research on available datasets. These datasets can be used for model training, or serve as reference for building custom DriveWise-specific datasets.
