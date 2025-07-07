2025-03-26 13:08

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# microservices architecture 🛠️
### information digest
- architecture that divide core functionalities into its own service
- services are flexible due its loose coupling relation with other services
- services are scalable due its independent manner
- it's complex to handle
- services hard relies on ci/cd automations and monitoring tools
- ideal for large applications and teams



### key words
- flexibility
- scalability
- resilience
- large and dynamic applications
- complexity
- deployment overhead
- fault-tolerant
- service mesh auxiliar technologies
- monitoring
- observability
- loosely coupled
- scale services horizontally independently



### overview
> Microservices Architecture (MSA) divides a system into small, independent services, each responsible for a specific business function. These services interact with each other over lightweight protocols like HTTP, RESTful APIs, or messaging queues. Each microservice can be developed, deployed, and scaled independently, providing flexibility, fault isolation, and making it easier to maintain complex applications.




### well suitable for
- where scalability and availability is needed
- e-commerce, scaling the payment service during holiday sales 
- streaming, scaling the recommendation engine during prime viewing times
- online banking, well suitable because services also enhances security and resilient systems
- saas products, it help scale



### key characteristics
- **small services**
- **independent deployment**: scale independently and ease maintaining
- **api or messaging queues communication**
- **data decentralization**: data autonomy and improve resilience
- **failure isolation**: reliability and enhance uptime



### benefits
- **scalability**
	- independent scaling
	- optimal performance, scale one without impact other service
- **flexibility**
	- ~~best-suited technology~~
	- each team can work independently
- **fault isolation**
	- because of the services independence, reliability
- ==enhance deployment==
	- because of the continuous delivery
	- and because of the frequent releases



### challengs/trade-offs
- **complexity**
	- orchestration overhead, it's hard to ensure that services communication work seamlessly
	- distributed system management, debugging is difficult due to the various distributed systems
- **deployment overhead**
	- ci/cd complexity, often this pattern requires robust ci/cd pipelines to manage
	- version management, can be harsh to maintain
- **monitoring and observability**
	- distributed tracing it's difficult. tools like OpenTelemetry, Jaeger, and Zipkin can help with this trace
	- track interactions is crucial for this pattern, understand the system health, monitor performance bottlenecks, and enhance reliability



### why this pattern increases reliability and enhance uptime of the system?
due to the fault isolation characteristic where one service fails it doesn't impact other services, and increasing reliability



### why this patterns is complex?
due to the services orchestration overhead and the difficult to debugging due to the distributed services form


### why micro services architecture relies heavily on monitoring and observability?
because of the distributed way of it. additionally, this pattern relies heavily on those in order to understand the system health, to monitor performance bottlenecks, and keep the system reliable



### what are service mesh technologies? what are some examples?
dedicated infrastructure layer for handling service-to-service communication. it's essencial for distributed systems. it provides traffic management, security, observability, and resilience



### why maintaining micro services is difficult?
actually it tends to be more easy due to the loosely couple way of it, but debugging can be difficult due to the inter-services communication. set up and run all together is hard. also, because it can be cumbersome to trace the right sequence of events
# References
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[02. source materials/articles/Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]