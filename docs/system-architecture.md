---
layout: page
title: System Architecture
---

# System Architecture

The Local Community Network (LCN) is a decentralised, offline-first system combining hardware, software, and local networking.

---

## Components

The system consists of four main components:

- **Raspberry Pi (Local Server)**  
  Hosts the application and creates a local Wi-Fi network  

- **Sensors (Weather Station)**  
  Collect environmental data such as temperature, humidity, and air quality  

- **Local Application (Frontend)**  
  Provides access to agriculture, weather, market, and community features  

- **Backoffice (Admin Interface)**  
  Enables content management and system configuration  

## System Overview
![System Architecture Diagram](../assets/images/system_architecture.svg)

## Data Flow
1. Sensors collect environmental data  
2. Data is processed and stored locally on the Raspberry Pi  
3. The application provides access to data through a local network  
4. Administrators manage content via the backoffice 

## Offline-first design
The system operates without continuous Internet access:
- local Wi-Fi network  
- local data storage  
- local access via browser  
This ensures accessibility in low-resource and connectivity-constrained environments.
