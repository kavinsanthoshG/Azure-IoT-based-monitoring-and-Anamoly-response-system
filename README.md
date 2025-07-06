# 🌐 Azure IoT-Based Monitoring and Anomaly Response System

This project demonstrates an end-to-end **Industrial IoT (IIoT)** solution designed for monitoring energy consumption across manufacturing machines and triggering anomaly-based alerts in real-time. Built as part of my **internship at [Nebeskie](#)** — an Industry 4.0 company — the system uses **Azure Cloud**, **X.509 device authentication**, **simulated telemetry**, and **event-driven automation** to mimic a real-world smart factory scenario.

---

## 📦 Features

- 🔐 **Secure Device Authentication** via X.509 Self-Signed Certificates (TLS)
- 🔁 **Simulated Real-Time Telemetry** (JSON Payload) in C#
- 📡 **MQTT Data Transmission** to Azure IoT Hub
- 📈 **Stream Analytics** to flatten and process telemetry
- 🧠 **Anomaly Detection Logic** (e.g., PowerFactorDrop, Energy Spike)
- 📊 **Time-Series Data Storage** using Azure Data Explorer (ADX)
- 📉 **Live Dashboards** with Azure Managed Grafana
- 🔔 **Automated Alerts** via Azure Functions & Logic Apps

---

## 📊 Simulated Telemetry Structure

Example JSON Payload:
```json
{
  "timestamp": "2025-06-30T16:44:20.085436+00:00",
  "factoryId": "chennai_fact",
  "location": "Chennai",
  "readings": [
    {
      "machineType": "OilExpeller",
      "voltage": 419.9,
      "current": 76.0,
      "activePower": 26.2,
      "powerFactor": 0.7,
      "energyConsumption": 0,
      "status": "Alert"
    }
  ],
  "totalActivePower": 81.3,
  "totalEnergyConsumption": 1.35
}

