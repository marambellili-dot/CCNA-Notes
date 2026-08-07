# Static Routing

## What is Static Routing?

A static route is a route manually configured by the network administrator. It tells the router where to forward packets for networks that are not directly connected.

---

## Why do we need Static Routes?

A router automatically knows only:

- Connected networks (C)
- Local interface addresses (L)

If a destination network is not present in the routing table, the router drops the packet.

Static routes allow the router to reach remote networks.

---

## Static Route Syntax

### Using the next-hop IP address

```bash
ip route <network> <mask> <next-hop>
```

Example:

```bash
ip route 192.168.2.0 255.255.255.0 10.0.12.2
```

---

### Using the exit interface

```bash
ip route <network> <mask> <exit-interface>
```

Example:

```bash
ip route 192.168.2.0 255.255.255.0 GigabitEthernet0/1
```

---

### Using both

```bash
ip route <network> <mask> <exit-interface> <next-hop>
```

Example:

```bash
ip route 192.168.2.0 255.255.255.0 GigabitEthernet0/1 10.0.12.2
```

---

# Default Route

A default route is used when no specific route matches the destination.

Syntax:

```bash
ip route 0.0.0.0 0.0.0.0 <next-hop>
```

Example:

```bash
ip route 0.0.0.0 0.0.0.0 10.0.12.2
```

---

## Routing Decision

The router checks routes in this order:

1. Specific route
2. Default route
3. Drop the packet if no route exists

---

## Key Points

- Static routes are manually configured.
- They allow communication with remote networks.
- A default route acts as a fallback route.
- Without a matching route or a default route, the router drops the packet.