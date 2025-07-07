2025-06-12 11:53

Status: #child

Tags: [[dev]] [[system-design]] [[interview]]

# System Design Interview - A Step-By-Step Guide
## introduction

interviews are stressful and we have little time to show what we are capable of

without a framework to follow it makes easy to waste time on things that don't matter. time is valuable during interviews

without a framework and with an unstructured interview, makes it hard to the interviewer to follow




## framework

the framework provides precious time by asking the right questions

it's good for 45-60 minutes interview session

we have 5 initial minutes of introduction

we have 5 last minutes on Q&A

the interview it's only to 35-45 minutes

suggested allocated time:
- step 1 (understand the problem and establish design scope) - 5 min.
- step 2 (propose high level design and get buy-in) - 20 min.
- step 3 (design deep dive) - 15 min.
- step 4 (wrap up) - 5 min.




## step 1 understand the problem (understand the problem and establish design scope)

the result the **step 1 (understand the problem and establish design scope)** is to come up with a **list of features to build** and the **non-functional requirements to satisfy**

### understand and establish scope

system design interviews announcements are quite vague

it's out job to organize the ideas and understand what we're building and what's important

⚠️ jumping right to the problem solution is a red flag 

ask as many questions that we want

_"why we're building it?"_

_"who is gonna to use it? who are our users? is it from mobile? is it a from online web application?"_

_"what are the mainly features we need to build?"_

we want to show the top features to build and make sure the interviewer agrees with it




## step 2 clarify (understand the problem and establish design scope)

### non-functional requirements

also consider non-functional requirements, but focus on **scale** and **performance**

the more senior the position is the more we need to show how we handle non-functional requirements

do a **roughly estimate** and **get a sense of the scale**




## step 2 framework (propose high level design and get buy-in)

top-down approach (client -> web server)

start with the api endpoints. the api's are the middle ground communication between the client and the server

don't propose endpoints that are not in our feature list

what are the api inputs? **field name, description, type**

what the response will look like?




## step 3 design diagram (propose high level design and get buy-in)

blueprint of the overall design

establish that the feature is being satisfied end-to-end

we commonly start with an api gateway nor a load balancer

establish the services to satisfy the functional requirements

introduce the data storage(database) layer




## step 4 design diagram (propose high level design and get buy-in)

don't mention other discussion points just yet. keep things like, failures scenarios, database scaling and high concurrency for later

don't mention non-functional requirements just yet

show the communication from client to server, load balancer, service, database for each item on the feature list

 

## step 5 data model schema (propose high level design and get buy-in && design deep dive && wrap up)

### propose high level design and get buy-in

design data modeling

stipulate read/write ratio

which database to choose

if the database modeling is the most important part of the app, extend the discussion to the deep dive design step




### deep dive design

this step is really open and has no "size fits all"

work with the interviewer to identify possible bottlenecks

here is where we expand the discussion on the non-functional features

articulate the problem

give at least two solutions

discuss trade-offs

pick up the solution and discuss with the interviewer




### wrap up

take some time to summarizes the design

highlight the uniques for particular situations

keep it short

leave enough room to ask the interviewer additional questions



# TRANSFORMAR ISSO EM UM PIECE OF WISDOM?
## faq

#### what's the difference between a api gateway and a load balancer as our first initial starting point on our high level design diagram?




# References
- [(YouTube) System Design Interview - A Step-By-Step Guide](https://www.youtube.com/watch?v=i7twT3x5yv8&t=4s&ab_channel=ByteByteGo)