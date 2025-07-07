2025-03-24 11:49

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# monolithic architecture 🏛️

> Monolithic architecture is a traditional approach where an application’s various components—such as the user interface, business logic, and database interactions—are combined into a single, cohesive unit

> good for smaller and less complex applications

> good for applications where the goal is to build quickly and with minimal overhead

> simplicity, lower infrastructure requirements, and quick deployment(?)

> suitable where the focus is to getting the product to the market quickly, without the need for extensive scaling or complex inter-component communication


- tightly couple
- less complexity
- good for MVPs, startups and prototyping (speed to the market)
- shares a single codebase and database
- it's difficult to scale
- it's difficult to transition to another architecture
- requires no costly infra structure
- due to the in process communication there's no network communication overhead
- low latency




### well suitable for
- MVPs (minimum viable product)
- legacy systems
- rapid prototyping
- startups and small teams
- when there's no immediate scaling needs
- when you need to speed to the market




### key characteristics
1. **single codebase**: all functionalities are inside the same codebase, reducing complexity
2. **centralized database**: causing performance bottlenecks
3. **tightly coupled components**: A change in one module can have cascading effects, causing the entire application to be redeployed




### benefits
1. **simplicity**: ==no complex inter-service communication required==.
2. **faster initial launch**: ==faster prototyping and getting a product to market quickly==.
3. **cost-effectiveness**:
4. **lower latency**: ==in-process communication between componenets==, so there’s ==no need for network overhead==, leading to ==reduced latency==.




### challenges/trade-offs
1. **scalability**: ==have to scale the entire system rather than specific components==. This can lead to ==inefficient resource use==.
2. **maintenance**: ==codebase grows==, **spaghetti code** and ==maintenance challenges==.
3. **limited flexibility**: ==new technologies tightly coupled nature of the application==.




# References

- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[02. source materials/articles/Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]
