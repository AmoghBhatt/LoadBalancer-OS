# Distributed Load-Aware Process Management System

A distributed master–worker based process management system developed for remote process execution, monitoring, migration, and load-aware task allocation across multiple worker nodes using TCP socket communication.

## 📌 Project Overview

This project simulates a distributed operating system environment where a central master node communicates with multiple worker nodes to manage processes remotely.

The system supports:
- Remote process execution
- Process monitoring and status tracking
- Process termination
- Simulated process migration
- Dynamic load-aware worker selection

## 🚀 Features

- 🖥️ Master–Worker distributed architecture
- 🌐 TCP socket-based communication
- ⚖️ Load-aware process scheduling
- 📊 Real-time CPU and memory monitoring
- 🔄 Simulated process migration between nodes
- 💀 Remote process termination
- 📋 Process status tracking
- 🧠 Automatic least-loaded worker selection
- 💻 Interactive command-line interface (CLI)

## 🛠️ Technologies Used

- Python
- Socket Programming
- Psutil
- JSON
- Subprocess Management
- TCP/IP Networking

## 📂 Project Structure

```text
project-folder/
│
├── master.py
├── worker.py
└── README.md
```

## ⚙️ System Architecture

### Master Node
The master node:
- manages worker communication
- selects least-loaded workers
- dispatches processes
- monitors cluster metrics
- handles migration requests

### Worker Node
Each worker node:
- executes assigned processes
- tracks running processes
- reports CPU and memory usage
- supports process kill and migration commands

## 🧠 Core Functionalities

### Process Execution
Processes can be remotely started on worker nodes using CLI commands.

### Load-Aware Scheduling
The master dynamically selects the least-loaded worker using:
- CPU utilization
- Memory utilization

### Process Monitoring
Workers continuously report:
- active processes
- system metrics
- process status

### Process Migration
The system simulates process migration by:
1. terminating process on source worker
2. restarting process on target worker

## ▶️ How to Run

### Start Worker Nodes

```bash
python worker.py 5001
```

```bash
python worker.py 5002
```

### Start Master Node

```bash
python master.py
```

## 💻 Supported Commands

```text
RUN <command>
RUN <command> --auto
STATUS ALL
STATUS <worker>
METRICS ALL
KILL <pid>
MIGRATE <pid>
EXIT
```

## 🎯 Learning Outcomes

- Understanding distributed systems architecture
- Implementing TCP socket communication
- Process lifecycle management
- Load balancing concepts
- Distributed process scheduling
- Remote system monitoring

## 👥 Contributors

Developed as a collaborative academic project.