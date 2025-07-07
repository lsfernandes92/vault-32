2025-04-07 16:22

Status: #child #adult 

Tags: [[dev]] [[system-design]]

# stream-based architecture 🚀
### information digest
- relies on data flow instead static batch data that are sent eventually
- good for real-time applications
- event-drive is the core of it
- monitoring is crucial
- IoT, financial, e-commerce, analytics apps
- choosing the right processing data stream tool is crucial
- managing state management is hard
- ensure data consistency, reliability and prevent duplication
- debugging is hard



### key words
- data flow
- low latency
- high-throughput
- decision on the fly
- real-time processing
- monitoring/observability
- data integrity
- prevent duplication
- replayability
- exactly-one semantics
- complex state management
- event-drive



### overview
> Stream-based architecture emphasizes real-time data processing, transforming how businesses handle continuous streams of data, as opposed to relying on static datasets. With this approach, data is processed as it moves, enabling systems to respond to events instantly and make decisions on the fly. This architectural style has found widespread use in fields like IoT, finance, e-commerce, and real-time analytics, where immediate action based on incoming data is crucial.




### well suitable for
- real-time applications
- IoT applications
- financial systems
- e-commerce systems
- analytics systems
- event monitoring systems
- system that requires reactivity(high-throughout and low-latency)



### key characteristics
- **data streams**: dynamic datasets
- **stream processing**: analyze and act on data. examples are Apache Kafka, Apache Flink, Apache Pulsar
- **event-drive architecture**: the core of it
- **windows**: logical time divisions used to aggregate or analyze data



### benefits
- **low latency**: decisions on the fly
- **scalability**: because its easy to horizontally scale
- **replayability**: stream can be reprocessed
- **work well with cloud providers** to visualize and analyze real-time insights



### challengs/trade-offs
- state management: use tools that leverages that 
- fault tolerance: grant data consistency, reliability and prevent duplications
- complex debugging



### why state management is so hard in this architecture?
distributed systems is per say hard to manage states, with data streamings is even hard



### what are the windows core concept?
windows are logical time divisions to aggregate or analyze data. types of windows:
- **tumbling windows**: fixed-size, non-overlapping windows
- **sliding windows**: overlapping windows that shift over time
- **session windows**: grouping data based on activity or session time



### why debugging can be difficult when using this architecture?
because the traditional debugging methods doesn't work for fast-moving data. so monitoring and observability tools are the essential. examples are confluent, grafana, and prometheus



### what's the replayability concept?
streams can be reprocessed to simulate past events



### what is exactly-one semantics and how to enable it?
is a data processing that guarantee that an event is processed exactly one time. and that prevent data duplication and data loss due to failures



### what are the tips for the developers?
- choose the stream processing tool
- aim for scalability
- implement exactly one semantics
- use monitoring and observability tools



### why continuous monitoring is so important for this architecture?
to keep low latency and optimal performance



### this architecture relies on another architecture. which one?
it hard relies on event-drive architecture



### what is the job of the apache flink?
it's job is to provide a mechanism for state management on distributed systems



### what are some techniques to grant data integrity and no data loss?
implement techniques such as the "checkpoints" on Kafka nor enable Kafka's durable storage so data remains safe during failures



### what are some well established tools for monitoring and observability?
Prometheus, Confluent and Grafana



### what tool should I use if I want high-throughtput and event pipeline?
Apache Kafka



### what tool should I use if I want complex state management?
Apache Flink



# References
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide 🛠️]]
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 2]]
- [[Mastering Essential Software Architecture Patterns A Comprehensive Guide🛠️, Part 3]]