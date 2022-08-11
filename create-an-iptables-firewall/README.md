# Create an iptables firewall

## Tasks
1- Create 4 network namespaces.

2- Namespaces are client1, client2, server, firewall

3- Create veth for all namespaces for network communication.

4- Serve sample http service inside the server namespace

5- Create iptables rules inside the firewall namespace and control traffic between the namespaces.

6- Rules

6.1- Client1 can ping to server

6.2- Client2 can access to server for http

6.3- Client2 can ping to firewall

6.4- Client1 doesn't have ping permission to firewall

### Notes

Client1 subnetwork is 192.0.2.0/26

Client2 subnetwork is 192.0.2.64/26

Server subnetwork is 192.0.2.128/26

Firewall should be a **stateful**.

### Topology
```
                 ┌─────────────────┐
                 │                 │
                 │    Firewall     ├───────┐
      ┌──────────┤                 │       │
      │          └───┬─────────────┘       │
      │              │                     │
      │              │                     │
      │              │                  ┌──┴───┐
      │              │                  │      │
      │              │                  │      │
┌─────┴────┐   ┌─────┴────┐             │Server│
│          │   │          │             │      │
│  Client1 │   │ Client2  │             │      │
│          │   │          │             │      │
└──────────┘   └──────────┘             └──────┘
```

