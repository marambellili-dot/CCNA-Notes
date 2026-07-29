# Routing Table Fundamentals

## What is a Routing Table?

A routing table is a database stored by a router. It contains routes to known destination networks and is used to determine the best path for forwarding packets.

---

## Route Types

### Connected Route (C)

- Automatically created when an interface is configured with an IP address and is up.
- Represents the entire directly connected network.
- Example:

```
C 192.168.1.0/24
```

Meaning:

> Send packets destined for the 192.168.1.0/24 network out the connected interface.

---

### Local Route (L)

- Automatically created for the exact IP address configured on an interface.
- Uses a /32 prefix because it represents only one IP address.
- Example:

```
L 192.168.1.1/32
```

Meaning:

> Packets sent to this IP are intended for the router itself.

---

## Packet Forwarding Process

When a router receives a packet:

1. Checks the destination IP address.
2. Searches the routing table.
3. Selects the best matching route.
4. Forwards the packet through the correct interface.

---

## Longest Prefix Match

If multiple routes match a destination, the router selects the most specific route (the route with the longest prefix length).

Example:

```
192.168.1.60
```

Matches:

```
192.168.1.0/24
```

instead of

```
192.168.0.0/16
```

because /24 is more specific.

---

## No Matching Route

If no matching route exists, the router drops the packet.

Unlike switches, routers do not flood packets.

---

## Switch vs Router

| Switch | Router |
|---------|---------|
| Uses MAC addresses | Uses IP addresses |
| Floods frames when destination MAC is unknown | Drops packets if no matching route exists |
| Works at Layer 2 | Works at Layer 3 |

---

## Key Takeaways

- Routing tables store known destination networks.
- Connected routes (C) represent directly connected networks.
- Local routes (L) represent the router's own interface IP addresses.
- Routers always perform a longest prefix match.
- If no route exists, the packet is dropped.