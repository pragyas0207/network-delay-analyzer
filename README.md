# 📡 Network Delay Analyzer (SDN Tool using Ryu)

## 🚀 Overview

The **Network Delay Analyzer** is a Software Defined Networking (SDN) tool that measures and analyzes network delay (latency) in real time using an SDN controller.

This project uses the Ryu controller along with Mininet to simulate a network and monitor packet delays across switches.

---

## 🎯 Features

* 📊 Real-time network delay monitoring
* 🔁 Packet-based delay estimation
* 🧠 SDN-based centralized control
* 🗂️ CSV logging for analysis
* 📈 (Optional) Graph visualization of delay trends
* 🌐 Works with custom Mininet topologies

---

## 🏗️ Project Architecture

```
Mininet (Network Emulator)
        ↓
   OpenFlow Protocol
        ↓
   Ryu Controller (Delay Analyzer)
        ↓
 Delay Calculation + Logging
        ↓
 CSV / CLI Output / Graphs
```

---

## 🛠️ Tech Stack

* Python 3.10
* Ryu (SDN Controller)
* Mininet (Network Emulator)
* OpenFlow Protocol
* Matplotlib (for visualization)

---

## ⚙️ Installation

### 1. Install dependencies

```bash
sudo apt update
sudo apt install mininet python3.10 python3.10-venv python3.10-distutils
```

---

### 2. Create virtual environment

```bash
python3.10 -m venv ryu-env
source ryu-env/bin/activate
```

---

### 3. Install Ryu

```bash
pip install --upgrade pip setuptools wheel
pip install ryu
```

---

## ▶️ Usage

### Step 1: Run the Ryu Controller

```bash
ryu-manager delay_monitor.py
```

<img width="940" height="262" alt="image" src="https://github.com/user-attachments/assets/d66e0a4e-6efb-4d35-9a29-76039c26368d" />

---

### Step 2: Start Mininet

```bash
sudo mn --topo single,3 --controller remote
```

<img width="940" height="562" alt="image" src="https://github.com/user-attachments/assets/ba6941e5-8d3f-4e65-b9ad-5bf0d19afbfa" />

---

### Step 3: Generate Traffic

```bash
mininet> pingall
```

<img width="631" height="216" alt="image" src="https://github.com/user-attachments/assets/98f8049d-7b3d-4192-bf1a-a1365f7a67fa" />

---

### Output

<img width="542" height="792" alt="image" src="https://github.com/user-attachments/assets/8cbc7239-f5c1-4eb2-af03-df61d0e3dbd0" />

---
### Wireshark

<img width="940" height="276" alt="image" src="https://github.com/user-attachments/assets/04bd68bc-b245-4e5d-8560-2f664636034e" />


<img width="940" height="453" alt="image" src="https://github.com/user-attachments/assets/6d8fa645-649e-46d8-8e7a-d83f8a0076c2" />


## 📂 Project Structure

```
network-delay-analyzer/
│
├── delay_monitor.py
├── README.md
```

---

## 📊 Future Improvements

* ⏱️ Accurate RTT-based delay measurement
* 🌍 Multi-switch delay mapping
* 📉 Real-time dashboard using Flask
* 🔔 Alert system for high latency
* ☁️ Cloud deployment (AWS)

---

## 💡 Use Cases

* Network performance analysis
* SDN research and experimentation
* Traffic optimization studies
* Educational tool for networking concepts


