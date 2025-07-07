2025-06-16 16:59

Status: #child 

Tags: [[dev]] [[system-design]] [[interview]]

# websocket

## overview

## keywords
- stateful connection
- long-lived connection
- bi-directional/two-way communication

## characteristics

websocket holds **stateful and persistent long-lived connection** between a client a server for their entire communication

websocket holds a **two-way/bi-directional** type of communication (greatly used on real-time applications)




## well suitable for

- real-time applications

## benefits?

## challenges/trade-offs

**challenge**
servers must have a persistent connection between client and server. that consumes resources (ram and tcp socket)

**solution**
use event-drive architecture or asynchronous frameworks to best handle the concurrent connections

--- 

**challenge**
horizontal scaling makes no sense bc it can cause connection and routing issues, like reconnect to another server

**solution**
sticky sessions and pub/sub systems (or message brokers) are needed if we want to scale

---

**challenge**
sending messages across all clients no matter which server node they're connected to

**solution**
sticky sessions and pub/sub systems (or message brokers) are needed to broadcast messages to all servers

---

**challenge**
if a server dies, all clients connected to them will lose their connection, causing a great spike of reconnections

**solution**
apply backoff and retry logic on client side

health checks and auto-scaling policies that gracefully drain connection before shutdown

allow client session re-attachment via token

--- 

**challenge**
sensitive to network drops (mobile networks)

**solution**
allow client session re-attachment via token

apply ping-pong (heartbeat) messages to detect network drops

# References
- [[websocket at scale]]
