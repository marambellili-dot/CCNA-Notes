# Switch Interfaces

## Overview

A switch interface connects network devices and defines how data is transmitted through the network.

## Interface Speed

Common interface speeds include:

- 10 Mbps
- 100 Mbps
- 1000 Mbps (1 Gbps)

Both devices should use compatible speed settings.

## Duplex Modes

### Half Duplex

- One device transmits at a time.
- Collisions may occur.

### Full Duplex

- Devices transmit and receive simultaneously.
- No collisions.
- Standard mode in modern Ethernet networks.

## Auto-Negotiation

Auto-Negotiation automatically selects the highest compatible speed and duplex between connected devices.

If one side is manually configured while the other uses Auto-Negotiation:

- Speed is usually detected correctly.
- Duplex defaults to Half Duplex.
- This may cause a Duplex Mismatch.

## Interface Status

Cisco interfaces can have different states:

- **up/up** → Interface is operating normally.
- **administratively down** → Interface disabled with `shutdown`.
- **down** → Physical connection is unavailable.

## Interface Counters and Errors

The `show interfaces` command displays:

- Interface speed
- Duplex mode
- Interface status
- Packet counters
- CRC errors
- Collisions
- Dropped packets

These statistics help troubleshoot network issues.

## Key Takeaways

- Configure matching speed and duplex on both ends.
- Prefer Auto-Negotiation when supported.
- Use `show interfaces` to monitor interface health.
- Check counters and errors when troubleshooting connectivity problems.