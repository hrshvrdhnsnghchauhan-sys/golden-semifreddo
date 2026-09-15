# ReUnite — Offline Mesh Rescue Network

ReUnite is an offline communication and disaster-relief concept designed to keep people connected when traditional communication infrastructure fails. During severe floods and other disasters, mobile towers, Wi-Fi networks, electricity, and internet connectivity can become unavailable. ReUnite addresses this problem by turning nearby smartphones into an offline peer-to-peer mesh network, allowing SOS signals and essential information to move from one device to another without depending on cellular networks or the internet.

## The Problem

During a disaster, communication can become one of the biggest challenges. When infrastructure goes offline, victims may not be able to contact emergency services or inform their families about their location. Rescue teams may also have limited visibility into where people need assistance.

ReUnite is designed around the idea that smartphones can continue communicating with nearby devices even when conventional networks are unavailable. The project focuses on creating a communication layer that can operate independently of cellular towers, Wi-Fi, internet connections, and centralized servers.

## How It Works

ReUnite uses a store-and-forward mesh communication approach. Nearby devices discover each other over Bluetooth Low Energy (BLE), allowing information to move between devices without requiring traditional network infrastructure.

The basic workflow is:

```text
User sends SOS
      ↓
Nearby devices discover the signal
      ↓
Signal is stored and relayed
      ↓
Multiple devices forward the information
      ↓
Rescue network receives the signal
      ↓
Rescuers identify high-density distress areas
```

The system is designed to support relay communication for up to eight hops. It can also maintain offline GPS breadcrumbs at regular intervals and synchronize information when devices come into contact with other nodes.

## Live SOS Map

The project includes an interactive map interface that visualizes SOS density, SOS signals, safe zones, and aid posts. A signal log provides an accessible text-based representation of the information displayed on the map. Users can select individual signals and locate them geographically.

The repository also provides a dedicated full-screen map interface through `map.html`. The map includes layer controls, signal logs, reset controls, and light/dark theme support.

## Key Features

* Offline peer-to-peer communication
* SOS signal broadcasting
* BLE-based device discovery
* Store-and-forward message relay
* Up to 8-hop relay depth
* Offline GPS tracking
* SOS density visualization
* Safe-zone and aid-post mapping
* Hazard pins for locations such as rising water and landslides
* Signal history and logging
* Accessible map information
* Light and dark interface themes

## Technical Specifications

ReUnite's proposed communication layer uses BLE 5.0+ and Wi-Fi Direct, with a target node range of approximately 100 meters outdoors under line-of-sight conditions. The design specifies a 0.3-second SOS interval, a 60-second GPS logging interval, encrypted unicast messaging, and a 3–5 day survival mode using throttled beacon polling. The intended infrastructure requirement is zero: no cellular network, Wi-Fi, internet connection, or server is required.

## Project Status

This repository currently represents a functional front-end prototype and demonstration of the ReUnite concept. The emergency signals displayed by the interface are simulated and should not be treated as real emergency information.

## Vision

ReUnite aims to demonstrate how everyday smartphones could become part of a resilient communication network during disasters. Its core principle is simple:

**When the network goes down, the devices around you become the network.**

The project can serve as a foundation for future development involving real mobile mesh networking, emergency communication, location sharing, disaster-response coordination, and resilient community networks.
