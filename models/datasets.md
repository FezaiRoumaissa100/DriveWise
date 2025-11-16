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

See: `activity-recognition/datasets.md` for detailed info.

---

## Summary Table

| Model | Dataset | Size | Format | Status |
|-------|---------|------|--------|--------|
| Traffic Sign Recognition | GTSRB | N/A | Images | ✅ Ready |
| Driver Behavior | DriverSVT | 600M+ samples | CSV | 📋 Queued |
| Driver Behavior | UAH-DriveSet | Multi-source | Video + Sensors | 📋 Queued |
| Driver Behavior | POLIDriving | N/A | Multi-source | 📋 Queued |
| Activity Recognition | Public Domain Activity | N/A | Sensors + GPS | 📋 Queued |
| Activity Recognition | Smartphone Behavior | N/A | Sensors + GPS | 📋 Queued |

---

## Usage Guidelines

1. **Select Dataset:** Choose dataset based on model type (see folder structure)
2. **Download:** Follow links to dataset sources
3. **Prepare:** Preprocess and split data (train/val/test)
4. **Document:** Update model README with dataset version and preprocessing steps
5. **Track:** Note any filtering or augmentation applied

---

## Next Steps

- Download and explore primary datasets (DriverSVT, UAH-DriveSet for behavior; GTSRB for traffic signs)
- Evaluate dataset suitability for DriveWise use cases
- Design preprocessing pipelines
- Document any licensing / attribution requirements

---

**Last Updated:** 2025-11-16  
**Status:** Preliminary research on available datasets. These datasets can be used for model training, or serve as reference for building custom DriveWise-specific datasets.
