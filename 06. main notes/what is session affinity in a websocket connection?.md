2025-06-20 12:34

Status: #adult 

Tags: [[dev]] [[system-design]] [[interview]]

# what is session affinity in a websocket connection?

#### what is session affinity?

session affinity make sure that the client always communicates with the same service server instance

it provides **stateful communications**, **no connection loss** and **connection consistency**




#### why session affinity is important when scaling websocket connections?

in a distributed environment where, for example, the load balancer manage the traffic from the client to the service server instances, session affinity guarantee that the client always communicates with the same service server instance

without this, each websocket handshake would route to different servers, and this breaks the websocket communication that said that only the original request server knows how to handle the request

for example, in a distributed environment, the client connects to the server A, then sends a text message, then the load balancer redirects to the server B that don't have the knowledge to handle it

with session affinity enabled the load balancer always route to the same server




# References

- [[websocket at scale]]
- [[websocket]]
