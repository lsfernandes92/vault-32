2025-03-10 12:21

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# the C4 Model - Visualizing Architecture 🌍

> It emphasizes simplicity, clarity, and collaboration, offering a visual approach to representing a system’s structure and interactions at various levels of abstraction.

> a popular choice due to its ability to convey complex software architectures in a way that is easy to understand.


- it gained popularity due it's simplicity, seamless collaboration between devs, stakeholders and non-technical people and clarity
- it have 4 layers of abstraction: context, container, component and code



> context diagram provides a broad view of the system, showcasing its relationship with external entities like users, other systems, or external services. The purpose is to understand the system’s boundaries and its primary interactions with the external world.

- context: focus on the boundaries and interactions with the external communications such as users, external apis, payment gateways, etc...
	- example: in an e-commerce platform, the context might be external apis, mobile clients, shipping providers, etc...



> This diagram decomposes the system into containers (applications or data stores).

- container: it decomposes into application or data stores
	- example: consider and e-commerce, the container could include web server, application server, relational database, etc...



>==broken down into components==. ==A component represents a module, service, or class that performs a specific function.

- component: a component represent a broken piece of the container that performs a specific action within the system
	- example: in an e-commerce platform, the component might include catalog service, the authentication component, shopping cart, order management, etc...



> provides detailed design information, mapping components to actual code structures

- code: it highlights the code structure and typically uses UML diagrams
	- example: in an e-commerce, might include a module or a class like `UserDAO`, `UserAuthentication`, etc..



### Advantages of using the C4 model

> - Clear communications
> - Collaborative
> - Evolving design
> - Scalability and Maintainability
> - Flexible notation

* it's simple: simplifies communication of complex architectures
* provides easy collaboration
* can evolve with future requirements
* identify potential NFR and areas of improvement
* it have some flexibility allowing teams to adapt as needed



### Best practices

> - Interactive diagram
> - Clear understanding without the need of additional explanation
> - Keep it simple, don't overcomplicate and focus on the key elements and relationships between them
> - Use version control to track changes as the system evolves
> - Legend and titles: ensure the diagram includes things to clarify the meaning of symbols

- use interactive and easy to reach tools like lucidchart or draw.io
- keep it simple
- make sure everyone understand the subtitles
- cersion control
# References

- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[software architecture who? 🏗️]]
- [[software design who? 🎨]]
- https://www.drawio.com
- https://www.lucidchart.com