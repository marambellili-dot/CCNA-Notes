# Lab 02 - Default Route

## Objective

Configure a default route to reach unknown networks.

## Commands Used

```bash
ip route 0.0.0.0 0.0.0.0 192.168.1.1

show ip route

ping 8.8.8.8
```

## Result

The router successfully forwarded packets using the Gateway of Last Resort.