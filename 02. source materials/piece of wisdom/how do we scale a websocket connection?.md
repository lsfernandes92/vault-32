2025-06-20 12:30

Status: #adult 

Tags: [[dev]] [[system-design]] [[interview]]

# how do we scale a websocket connection?

#### some design may want a real-time two-way communication between server and client. a common solution is websocket. in websocket solution we need to establish multiple and stateful communications between the client and one server. in this scenario, how do we scale?

sticky sessions and pub/sub systems (or message brokers) are needed if we want to scale and broadcast messages across server nodes




# References

- [[websocket at scale]]
- [[websocket]]
- [[what is session affinity in a websocket connection?]]
