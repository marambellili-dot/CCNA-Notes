# IPv4 Fundamentals

## What is IPv4?

IPv4 is a logical addressing system used to identify devices on a network.

Example:

192.168.1.10

## IPv4 Structure

An IPv4 address contains 32 bits divided into four octets.

Example:

192.168.1.10

## Network and Host Portions

An IPv4 address is divided into:

- Network Portion
- Host Portion

The network portion identifies the network.

The host portion identifies a device inside that network.

## Subnet Mask

The subnet mask determines which part of the address belongs to the network and which part belongs to the host.

Example:

IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0

## Number of Hosts

The number of available hosts depends on the number of host bits.

Formula:

Hosts = 2^n - 2

where n is the number of host bits.

## Basic Cisco Configuration

Configure an IP address on an interface:

```cisco
enable
configure terminal

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
```

Verify configuration:

```cisco
show ip interface brief
```

## What I Learned

- Structure of IPv4 addresses.
- Difference between network and host portions.
- Purpose of subnet masks.
- Host calculation basics.
- Basic IP configuration on Cisco devices.