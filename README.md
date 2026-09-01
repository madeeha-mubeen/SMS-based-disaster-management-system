# ResQLink — SMS-Based Disaster Coordination.

<p align="center">
  <strong>Offline-First Emergency Communication & Disaster Response Coordination System</strong>
</p>

<p align="center">
  <a href="https://ideathon-eight-ruddy.vercel.app/">
    <img src="https://img.shields.io/badge/Live%20Demo-4F46E5?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
  <img src="https://img.shields.io/badge/Status-Prototype-6D28D9?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Focus-Disaster%20Response-4338CA?style=for-the-badge"/>
</p>

---

## Overview

**ResQLink** is an offline-first emergency communication and disaster coordination system designed for situations where internet connectivity and conventional communication infrastructure may be unavailable.

The system provides multiple communication channels, including **SMS simulation, mesh-network simulation, and local beacon portals**, allowing emergency requests to reach appropriate responders through alternative communication mechanisms.

Requests from different channels are collected and presented through a **unified command dashboard**, helping response teams process, prioritize, and coordinate emergency situations more efficiently.

> The project was developed by **Team Meraki**.

---

## Problem Statement

During natural disasters such as **floods, earthquakes, and cyclones**, communication infrastructure can become damaged or completely unavailable.

This creates a critical communication gap between affected individuals and emergency responders.

Key challenges include:

- Internet and mobile networks may be unavailable
- Emergency requests may not reach authorities on time
- Rescue teams may lack centralized coordination
- Multiple communication sources may be difficult to manage
- Responders may not have a unified view of incoming requests

ResQLink addresses these challenges by providing a decentralized, offline-capable approach to emergency communication.

---

## Solution

ResQLink provides a **multi-channel emergency communication system** designed to operate without depending entirely on internet connectivity.

The system can:

- Accept emergency requests through SMS simulation
- Simulate communication through a mesh network
- Provide a local beacon portal for structured emergency requests
- Automatically categorize incoming requests
- Assign requests to appropriate response teams
- Store information locally
- Synchronize and normalize requests across modules
- Display requests through a unified command center
- Provide filtering, search, and request-status tracking

This approach aims to improve **response speed, coordination, and emergency request management**.

---

## System Architecture

```text
                         ┌─────────────────────────┐
                         │      Emergency User     │
                         └────────────┬────────────┘
                                      │
                    ┌─────────────────┼─────────────────┐
                    │                 │                 │
                    ▼                 ▼                 ▼
             ┌────────────┐    ┌─────────────┐   ┌─────────────┐
             │     SMS    │    │ Mesh Network│   │   Beacon    │
             │  Dashboard │    │  Simulator  │   │   Portal    │
             └──────┬─────┘    └──────┬──────┘   └──────┬──────┘
                    │                 │                 │
                    └─────────────────┼─────────────────┘
                                      ▼
                         ┌─────────────────────────┐
                         │ Request Processing &    │
                         │ Team Assignment         │
                         └────────────┬────────────┘
                                      │
                                      ▼
                         ┌─────────────────────────┐
                         │      Local Storage      │
                         │       LocalStorage      │
                         └────────────┬────────────┘
                                      │
                                      ▼
                         ┌─────────────────────────┐
                         │    Unified Dashboard    │
                         │                         │
                         │ Search · Filter · Status│
                         │ Tracking · Coordination │
                         └────────────┬────────────┘
                                      │
                                      ▼
                         ┌─────────────────────────┐
                         │    Emergency Responders │
                         └─────────────────────────┘
