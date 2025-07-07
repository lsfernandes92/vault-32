2025-03-15 09:49

Status: #child #adult

Tags: [[dev]] [[system-design]]

# event-drive architecture ⚡
> Event-Driven Architecture (EDA) is a design paradigm centered around the idea that the flow of operations is dictated by events—specific changes in state within a system
- it's an architecture where the events dictates the data flow



> user actions, system state transitions, or external stimuli, act as triggers for subsequent actions.
- interactions with user and payment providers and examples that triggers the event producing, distribution and processing



> highly suited for systems that need to process and respond to ==real-time== events in an ==asynchronous manner==, making it ==ideal for use cases like financial transactions, IoT systems, or social media platforms.
- make well suitable for real-time systems



### Well-suited for
- financial transactions
- systems that requires asynchronous operations
- systems that requires decoupling between services
- IoT systems
- social media
- game platforms
- monitoring systems
- trading platforms
- microservices communications



### Key Characteristics
- Loosely couple
- Asynchronous communication
- Scalability
- Reactivity



### Benefits
1. **Flexibility**
	- independent scaling of components without impacting others
	- Easy to add or remove services, enabling rapid changes or additions to the system
2. **Performance**
	- Asynchronous processing allows for efficient resource allocation. Since events are processed in parallel, the system can handle high loads and scale as needed
	- suitable for low-latency and high-throughput systems requirements
3. **Real-time operations**
   
- flexibility due to the loosely couple fact in the event broker layer
- asynchronous operations
- performance due to components that can scale independently and also due to the asynchronous operations
- enable real-time operations



### Challenges/Trade-offs
1. **Complexity**
	- **Debugging**: ==Asynchronous communication== can ==obscure the order in which events are processed==, making it ==harder to trace errors==
	- **Event flow managament**: Ensuring ==events are processed in the correct order==, especially in complex systems, can be challenging.
2. **Data integrity**
	- Delays or missed events can disrupt system consistency and event duplication also poses a risk, which can be mitigated using ==idempotent consumers.==
3. **Infrastructure**
	- relies heavily on the broker like Kafka or RabbitMQ. Ensuring message delivery and fault tolerance in brokers is critical.

- complexity in debugging and due to the asynchronous nature
- hard rely on event broker, so build the broker carefully aiming fault tolerance and the correctness sequence of the events are essential
- ensure the correctness sequence of the events is crucial and specially difficult in large systems



# References
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[02. source materials/articles/Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]
