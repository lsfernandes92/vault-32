w2025-03-28 18:00

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# serverless architecture 🌐
### information digest
- no need to provision or maintaining server, and instead focus on develop the core business
- the service provider deals with performance, availability and scalability
- scalability can be on-demand and automatic
- good if you want to speed to the market
- cold starts, where the provider needs to allocate resources and start the server are bad for time-sensitive systems
- works well in conjunction with event-drive architecture. events, user interactions, database updates triggers the function execution
- function execution time is sometimes a issue
- verdor lock-in is a problem that can be mitigated using portability in mind when developing systems
- cost-efficiency due to the no idle time and it avoids over-provisioning



### key words
- faster time to the market
- on-demand/auto scale
- cost-efficiency
- vendor lock-in
- limited execution time
- no need to maintain nor provision the server
- cold start



### overview
> Serverless Architecture is a cloud-computing model where developers build and run applications without managing servers. In this model, ==cloud providers== automatically handle the ==infrastructure, scaling, and maintenance== required to run applications. Serverless computing ==abstracts the underlying server management==, allowing developers to ==focus on writing code for business== logic rather than worrying about hardware resources.




### well suitable for
- mobile and web apps
- real time systems
- IoT systems
- if you need speed to the market
- if you need to scale quickly



### key characteristics
- **no server management**: no maintaining and provision
- **event-drive**: interactions triggers function exection
- **automatic scaling**: allocate resources neither on sudden spike nor reduced traffic
- **pay as you go**: measured by number of function invocations and execution time



### benefits
- **cost-efficiency**
	- no idle time: not using = no need for a server instance
	- cost control: avoid over-provisioning resources
- **scalability**
	- on demand and automatic: allocated resource on sudden spike nor reduced traffic
- **faster time to the market**
	- simplified deployment
	- focus on code core business
- **fault tolerance and reliability**
	- cloud provider automatically deals with failover and backup, and that's increase availability
	- server are like CDN in terms of geographical location



### challengs/trade-offs
- **cold-start**: latency on first request
- **hard for debugging and monitoring**: many events and function that are hard to track. use cloud provider monitoring tools like AWS CloudWatch and Google Stackdriver
- **vendor lock-in**: dependency of the cloud provider. try to design applications with focus on portability
- **limited execution time:** AWS Lambda functions have maximum execution time of 15 minutes. try to use task queue and break long-running task into smaller ones



# References
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[01. rough notes/Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]
- [[event-drive architecture ⚡]]