# 🔧 Predictive Maintenance — Industrial Anomaly Detection

> Detecting machine failures before they happen using unsupervised ML on industrial sensor streams — built for automotive production environments.

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)

---

## 📋 Project Overview

Unplanned downtime in automotive production can cost €10,000–€50,000 per hour. This project implements real-time anomaly detection on industrial sensor data to enable **predictive maintenance** — flagging equipment issues before a breakdown occurs.

**Scenario:** A robotic welding station in an automotive assembly line. Five sensors stream data every 10 minutes. The model must detect early signs of bearing wear, overheating, or pressure failures.

---

## 🎯 Results

| Model | Precision | Recall | F1 |
|---|---|---|---|
| Isolation Forest | ~0.85 | ~0.90 | ~0.87 |
| Local Outlier Factor | ~0.80 | ~0.85 | ~0.82 |

**Isolation Forest preferred** — higher recall means fewer missed failures (critical in safety environments).

---

## 🔍 Sensor Features

| Sensor | Unit | Anomaly Signal |
|---|---|---|
| Vibration | mm/s | Bearing wear → high vibration |
| Temperature | °C | Overheating → temperature spike |
| Current | A | Motor stress → overcurrent |
| Pressure | bar | Hydraulic leak → pressure drop |
| Rotation speed | RPM | Mechanical fault → speed deviation |

---

## 🛠️ Tech Stack

- **Python** — pandas, numpy, matplotlib
- **Anomaly Detection** — IsolationForest, LocalOutlierFactor (scikit-learn)
- **Evaluation** — Precision, Recall, F1, Confusion Matrix, ROC-AUC
- **Visualization** — Real-time anomaly score timeline

---

## 🚀 Getting Started

```bash
git clone https://github.com/Razafindriatsara/predictive-maintenance
cd predictive-maintenance
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook predictive_maintenance.ipynb
```

---

## 🏭 BMW Relevance

- Directly applicable to BMW's Werk München, Werk Dingolfing, Werk Regensburg
- Supports BMW Plant Intelligence and Industry 4.0 digitalization strategy
- Foundation for integration with BMW's MES (Manufacturing Execution System)
- Can be extended with streaming data pipelines (Kafka, Azure IoT Hub)
