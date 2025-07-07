2025-04-28 10:53

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# strangler fig pattern 🌳
### information digest
- modernization
- good pattern for stack migration
- don't disrupt the entire system
- api gateway
- identify/build/redirect traffic/decommission
- gradual and incremental



### key words
- replacement of legacy systems
- gradual and incremental
- reduced risk
- no downtime to legacy 
- testing/documenting throughout process
- modernize
- api gateway/proxy



### overview
> The **Strangler Fig Pattern** is a widely recognized approach in software design that facilitates the gradual replacement of legacy systems. Its inspiration comes from the strangler fig tree, which over time grows around and replaces its host tree. This method allows organizations to modernize their systems piece by piece without the need for large-scale, disruptive overhauls. By gradually phasing out legacy components, it ensures that business operations can continue uninterrupted ⚙️



### well suitable for
- legacy systems
	- performance issues
	- need to scale
	- be compatible with modern techs
- modernization
	- monolith into microservices
- cloud migration



### key characteristics
- gradual and incremental
- minimum risk
- no downtime and interruption
- modernization
- high-level steps
	- evaluate func.
	- test and develop
	- redirect traffic
	- decommission legacy code



### benefits
- ==minimum risk involved==, legacy code intact until the new one is fully tested
- ==no downtime==
- ==modernization==, easier to introduce new tech with the gradual approach
- ==resource efficiency==, because you focus on smth



### challengs/trade-offs
- ==dual system management==, systems have different arch, techs, etc...
- ==integration overhead==, api gateway or proxy = new layer of complexity
- ==performance concerns==, redirection of traffic = additional latency




### what are the transitions core concepts involved in this pattern?
- ==analyze the legacy system==
	- evaluate the func.
	- document dependencies
	- assessing riks
- ==develop the new functionality==
	- choose the modern tool
	- build with modularity
	- test
- ==integrate the new system==, redirect traffic to:
	- api gateway
	- proxy
- ==test incrementally==
	- unit and integration test
	- a/b testing
	- monitoring
- ==phase out the legacy code==
	- decommission legacy code
	- final test



### why do we minimize the risks using this approach?
bc. legacy code remains intact until the new system is fully tested and integrated. also bc. large system overhaul poses the risk of failure and the gradual approach reduce these issues



### what can we do to analyze the legacy systems properly?
- evaluate the func.
- seek for dependencies and document it
- assess risks



### how do we integrate the new system?
we do that by split and redirecting the traffic to either the new and the legacy system, and we do that by using either api gateways nor proxy



### what are some techniques to gradually increment the changes and test it? (nginx)
once the new system is ready, use nginx as an api gateway to redirect api calls to the new microservice



### what are the testing techniques that you could apply? mention some tools examples
- unit and integration tests
- a/b testing, route small portion of traffic
- monitoring using tools like prometheus and grafana



### why nginx is not consider an api gateway?
nginx is consider a basic api gateway using features like load balancing and reverse proxy, although it lacks api monetization (where u can set billing prices for api usage); and developer portal (where devs might discover apis, manage api keys, test api, etc...)



### why testing is so important for this pattern specific?
it's a way to document things, and because it guarantee that nothing breaks between old and new system transition



### what are some tools that support the strangler fig pattern?
- api gateways
	- nginx
	- apigee
	- aws api gateway
- proxy
- monitoring
	- grafana
	- prometheus
- service meshes
	- istio
	- linkerd
- ci/cd
- github actions



### what are some examples of tool for api gateway?
- nginx
- aws api gateway
- apigee
- kong



### what are service meshes?
it's a dedicated infrastructure layer that manages communication between distributed systems in a cloud-native environment. it provides:
- traffic control, load balancing, routing, a/b testing
- observability, metrics, logs, services traces
- security, authentication and authorization
- resilience, retires, timeout, and circuit breaks




# References

- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 3]]