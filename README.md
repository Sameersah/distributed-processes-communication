# gRPC Shared Memory Coordination System (Mini 2)

## 📌 Overview

This project is part of CMPE 273's Mini 2 assignment. It demonstrates a distributed system consisting of multiple processes communicating across multiple machines using **gRPC** and **shared memory**, designed in an **overlay tree structure**.

The system features:
- Multi-language gRPC (C++ server, Python/C++ clients)
- Asynchronous communication across a process network
- Shared memory for intra-machine data exchange
- Transactionless caching to improve performance
- A single public portal (Process A) handling all external client queries

---

## 🧠 Concepts Explored

- Shared Memory (POSIX `shm_open`, `mmap`)
- gRPC Inter-Process and Inter-Machine Communication
- Asynchronous Servers in C++
- Overlay Tree Design & Query Routing
- Caching Mechanisms (in-memory)
- Multi-language system (C++ & Python)

---

## 🧱 Architecture

### ➤ Process Layout

A
|
B
/ \
C   D
    \
     E



- **Process A**: Public entry point (portal)
- **Processes B–E**: Internal data contributors
- Each process has edges (peers) defined in `overlay_map.json`

---

### ➤ Technology Stack

| Component      | Technology |
|----------------|------------|
| Communication  | gRPC       |
| Languages      | C++, Python |
| Shared Memory  | POSIX `shm_open`, `mmap` |
| Build System   | CMake      |
| Testing        | Shell scripts, unit tests |
| OS             | Linux/Unix or macOS |

---

## ⚙️ Setup & Installation

### 1. Clone the Repo

```bash
git clone https://github.com/<your-username>/grpc-shared-memory-coordination.git
cd grpc-shared-memory-coordination

2. Install Dependencies
gRPC and Protocol Buffers

CMake

Python 3

gRPC C++ Setup (Ubuntu/Mac)
[Insert gRPC C++ install guide link or command snippet here]

Python

```
pip install grpcio grpcio-tools

```


