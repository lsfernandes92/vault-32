2025-05-30 11:32

Status: #child 

Tags: [[oop]] [[dev]] [[ruby]]

# composition vs inheritance
## why prefer composition over inheritance?

**inheritance is tight coupling**. change the parent class and the changes echoes through all the child classes
**composition** works with loose coupling **independent objects**

**inheritance** has a **fragile base class** and composition has no parent class

**inheritance** is **difficult to test or override parts**. on the other hand, **composition** has independent objects that can be **reuse anywhere** and **swap out components easily** making it **an flexible approach and easy to test**

with **composition** you have **focused and encapsulated objects** that aligns with the single responsibility principle and **avoid bugs compared to deep inheritance trees**


# References
- [[composition]]
- [[inheritance]]
- [[OOP concepts]]