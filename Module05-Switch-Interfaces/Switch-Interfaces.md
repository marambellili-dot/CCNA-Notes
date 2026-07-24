# Switch Interfaces

## Overview

Switch interfaces connect network devices and operate using two main parameters:

- **Speed**: Defines the transmission rate (10, 100, or 1000 Mbps).
- **Duplex**: Defines how data is transmitted.

## Duplex Modes

- **Half Duplex:** Devices send or receive data, but not at the same time.
- **Full Duplex:** Devices can send and receive simultaneously with no collisions.

## Auto-Negotiation

Auto-Negotiation allows two connected devices to automatically agree on the highest supported speed and duplex settings.

## Duplex Mismatch

If one device uses Auto-Negotiation and the other is manually configured:

- The speed can usually be detected.
- The duplex defaults to **Half Duplex**.

This creates a **duplex mismatch**, which can cause:

- Collisions
- Packet loss
- Poor network performance

## Key Points

- Auto + Auto → Best Speed + Full Duplex
- Manual + Manual → Matching configuration required
- Auto + Manual → Speed detected, Duplex becomes Half Duplex