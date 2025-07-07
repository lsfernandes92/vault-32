2025-04-03 17:54

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# service-oriented architecture(SOA) 🛠️
### information digest
- used for larger apps
- good for decouple monolith applications
- interoperability
- reusability
- scalability
- similar to micro services, but with differences
- services communicate seamlessly with each other
- network overhead and constant service communication performance issue
- there's the concept of service providers, service consumers, service registry



### key words
- decentralization
- communication via network
- scalability
- flexibility and adaptability
- interoperability
- reusability
- core components are service providers, consumers, and registry
- legacy system modernization
- large systems
- enhanced collaboration



### overview
> Service-Oriented Architecture (SOA) is an architectural approach that organizes software systems into a series of loosely coupled and self-contained services. Each service is responsible for executing a specific business function, and services communicate with each other via a network using standardized protocols. This design allows various systems to collaborate seamlessly, even when they are built using different technologies or platforms.




### well suitable for
- **legacy systems modernization**:  
	- good for wrapping existent functions into services, and preserving the old core structure
	- don't require complete overhaul
- **enterprise systems**: 
	- ideal for large-scale enterprise systems, such as CRM and ERP
	- provides smooth communication between business areas
	- provides flexibility to evolve
- **multi-channel systems**: 
	- support multiple platforms such as web app, mobile app, and IoT devices
	- this allows ease scale and adaptability(provides interoperability and reusability between services)



### key characteristics
- decentralization of functions, core business, databases, etc..
- communication via network standardized protocols and well-defined interfaces
- flexibility and adaptability


### benefits
- **reusability**
- **interoperability**: heterogeneous systems nor modernization of legacy systems
- **scalability**
	- scale independently
	- one service can handle increased load without affecting others services
- **enhanced collaboration**
	- enhance collaboration between teams
	- team can focus on their area of expertise



### challengs/trade-offs
- **orchestration**:
	- managing middleware, such as an ==Enterprise Service Bus== (ESB), can add complexity to the system
	- requires additional configuration and monitoring to smooth integration between services
	- ==RabbitMQ== and ==Kafka== can simplify the communication between services
- **monitoring and governance**
	- monitoring tools is the key to track performance and seamlessly communication between services. example tools: ==Prometheus== and ==Dynatrace==
- **performance issue**
	- network communication/latency = less performance



### whats the main differences between SOA and micro-services architecture?

# References
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 3]]