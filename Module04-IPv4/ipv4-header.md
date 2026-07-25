# IPv4 Header

## Overview

The IPv4 header contains control information used by routers and hosts to correctly deliver packets across networks.

## Main Fields

- Version
- IHL (Header Length)
- DSCP / ToS
- Total Length
- Identification
- Flags
- Fragment Offset
- Time To Live (TTL)
- Protocol
- Header Checksum
- Source IP Address
- Destination IP Address
- Options (optional)

## Important Fields

### Version

Indicates the IP version (IPv4).

### Total Length

Specifies the total packet size.

### TTL

Limits the lifetime of a packet to prevent routing loops.

Each router decreases the TTL by one.

If TTL reaches zero, the packet is discarded.

### Protocol

Specifies the upper-layer protocol carried inside the packet.

Examples:

- TCP
- UDP
- ICMP

### Source Address

IPv4 address of the sender.

### Destination Address

IPv4 address of the receiver.

## What I Learned

- Every IPv4 packet begins with a header.
- Routers inspect the IPv4 header to determine where packets should be forwarded.
- TTL prevents packets from circulating forever.