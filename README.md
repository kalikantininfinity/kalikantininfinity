# Hi, I'm Kalikant Jha

> *Most engineers build software that lives in the cloud. I build software that has to survive contact with the ground.*

CS student at **Arkansas State University** pursuing AI/MLOps and Robotics Engineering.
My real classroom is a self-funded robot on my desk — I learn by making the thing, breaking the thing, and rebuilding it better.

I'm a builder before I'm anything else. Each project is a brick: reusable, documented, compounding into a stack I own end to end.

---

## What I'm Building

### AMDVS — Autonomous Multi-Domain Vehicle System

A self-funded autonomous ground rover built from a bare board. No lab, no grant, no team.

The goal isn't a demo that looks smart — it's a system that **stays smart when a sensor lies, the sun blinds the camera, or the path disappears.**

**Phase 1 — Ground Rover (Active)**

| Component | Detail |
|---|---|
| Compute | NVIDIA Jetson Orin Nano Super 8GB |
| Detection | YOLOv8n → TensorRT FP16 engine |
| Performance | **30 FPS steady-state**, on-device |
| Camera | Arducam IMX219 CSI |
| OS / SDK | Ubuntu 22.04 · JetPack 6.2 · CUDA 12.6 |
| Nav Stack | ROS 2 / Nav2 |
| Chassis | Hiwonder double-layer tracked |

**Build Milestones**

```
✅ GP-1  Real-time object detection — YOLOv8n @ 30 FPS on CSI camera (verified)
→  GP-2  Lane following
   GP-3  GNSS + IMU waypoint navigation (dual-EKF: fast/drifting + GPS-corrected)
   GP-4  360° LiDAR mapping
   GP-5  Concurrency — asyncio + ROS 2
   GP-6  Hardware e-stop reflex (<50ms watchdog, ATmega328P)
```

**Phase 2 — Cooperating Drone**

A drone that scouts ahead and docks back on the rover for recharging — the Perseverance + Ingenuity idea, built in a bedroom. Precision docking via AprilTag/ArUco fiducials.

**Architecture Principle**

```
Reflex / Safety Layer   ← deterministic, never depends solely on Jetson
        ↓
Perception              ← YOLO / OpenCV on Jetson
        ↓
Navigation / Control    ← ROS 2 / Nav2
        ↓
Strategic Reasoning     ← LLM, advisory only, never in real-time loop (Phase 2+)
        ↓
Human Interface         ← voice / dashboard (Phase 2+)
```

The LLM is **never** in the real-time control loop. The hardware e-stop is a from-the-start requirement, not a deferred feature.

---

## Stack

**Robotics & Embedded**
`ROS 2 / Nav2` `NVIDIA Jetson / JetPack` `TensorRT` `CUDA` `Sensor Fusion / EKF` `LiDAR` `GNSS` `IMU` `Hardware Watchdog (ATmega328P)`

**AI / ML & Vision**
`YOLOv8` `TensorRT FP16` `OpenCV` `jetson-utils` `PyTorch` `AprilTag / ArUco`

**Software**
`Python` `asyncio` `Linux (Ubuntu 22.04)` `Git` `Flask` `WebSocket` `4G / LoRa / Iridium comms`

**CS Fundamentals**
`Data Structures` `Algorithms` `Computer Architecture` `RISC-V Assembly` `DSA`

**Learning Now**
`MLOps` `RAG` `Agentic AI` `Python DSA`

---

## How I Build

**Safety is not deferred.**
The unglamorous layer — safety reflexes, sensor fusion, the code that keeps an autonomous system alive when reality stops cooperating — that's the interesting work. A sub-50ms hardware e-stop is a day-one requirement.

**Self-funded means every decision counts.**
No lab, no grant, no team. That constraint forces prioritization, documentation, and real engineering over demos.

**Each project is a brick.**
Reusable, documented, compounding. No black boxes I can't explain or rebuild.

---

## CS Coursework @ Arkansas State University

- **Data Structures** — hash tables, red-black trees, Dijkstra's algorithm, dynamic programming
- **Computer Architecture** — RISC-V assembly, CPU performance, two's complement, Patterson & Hennessy
- **Physics** — momentum/collisions, rotational mechanics
- **AI/MLOps track** — Computer Vision → MLOps → RAG → Agentic AI

---

## What I'm Looking For

Teams building **autonomous systems**, **perception**, or **embedded AI** — the places where code meets physics and "it works on my machine" isn't good enough.

If you've ever debugged why a robot froze at 2am, we'll get along.

---

## Links

- 🌐 [kalikantjha.com](https://kalikantjha.com)
- 💻 [github.com/kalikantininfinity](https://github.com/kalikantininfinity)

---

<sub>AMDVS · Self-funded · Built ground-up · No shortcuts.</sub>