# 🚀 AI Self-Healing Cloud Monitoring System

An intelligent, real-time cloud monitoring dashboard that not only **detects anomalies** but also **automatically heals systems** — transforming traditional monitoring into an **autonomous control system**.

---

## 🧠 Overview

This project implements a **self-healing cloud architecture** that continuously monitors multiple servers using Prometheus, detects anomalies in CPU, RAM, and Disk usage, and performs automated recovery actions via SSH.

It also provides a **modern interactive dashboard** for real-time visualization and system insights.

---

## ⚡ Key Features

* 📊 **Real-Time Monitoring**

  * Tracks CPU, RAM, and Disk usage using Prometheus
* 🧠 **Anomaly Detection**

  * Detects threshold breaches and unusual spikes
* 🔧 **Automated Healing**

  * Restarts services or resolves issues via SSH
* 📜 **Healing History**

  * Logs all actions with timestamps and metrics
* 🌐 **Interactive Dashboard**

  * Live system map with selectable instances
* 🎯 **Per-Server Graph Monitoring**

  * Click any server → view its real-time metrics
* 🔮 **Prediction System**

  * Detects rising trends before failure
* 📡 **Live Status Indicator**

  * Instant visual + audio feedback for anomalies

---

## 🏗️ Architecture


Prometheus + Node Exporter
        ↓
Python (detect.py)
        ↓
Automated Healing (SSH)
        ↓
JSON + CSV Logs
        ↓
Interactive Dashboard (HTML + JS)



## 🛠️ Tech Stack

* **Backend**

  * Python
  * Paramiko (SSH automation)
  * Prometheus (metrics)
* **Frontend**

  * HTML, CSS, JavaScript
  * Chart.js (visualization)
* **Infrastructure**

  * AWS EC2 Instances
  * Node Exporter


## 🚀 How It Works

1. Prometheus collects metrics from all servers
2. `detect.py` fetches and analyzes metrics
3. If anomaly detected:

   * System triggers healing via SSH
4. Results are logged in:

   * `status.json`
   * `healing_history.csv`
5. Dashboard reads and displays data in real-time



## 📸 Dashboard Highlights

* 🟢 Live system health monitoring
* 🔴 Automatic anomaly alerts
* 📊 Multi-metric graph (CPU, RAM, Disk)
* 🖱️ Click-based server selection
* ⚡ Real-time updates without refresh



## ⚙️ Setup Instructions

### 1. Start Prometheus

```bash
./prometheus
```



### 2. Run Monitoring Script

```bash
python detect.py
```


### 3. Launch Dashboard

```bash
python -m http.server 8000
```

Open:

```
http://localhost:8000
```

---

## 🧪 Demo Scenario

* Increase CPU load on a server:

```bash
yes > /dev/null &
```

* System will:

  * Detect anomaly ⚠️
  * Trigger healing 🔧
  * Update dashboard in real-time 📊


## 🎯 Key Highlights

* Cloud-agnostic (AWS, Azure, local VMs)
* Fully automated monitoring + recovery
* Interactive and user-friendly dashboard
* Real-time decision-making system

---

## 🔮 Future Improvements

* 🤖 Machine Learning-based anomaly prediction
* 🌐 Deployment with FastAPI + Next.js
* 🔐 Authentication & multi-user dashboard
* 📊 Advanced analytics & alerts

---

## 👨‍💻 Author

**Garv Kapoor**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share feedback!
