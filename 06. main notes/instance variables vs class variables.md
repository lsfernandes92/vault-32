2025-05-30 11:55

Status: #child 

Tags: [[oop]] [[dev]] [[ruby]]

# instance variables vs class variables

the difference relies on **who owns them** and **how they are shared**




#### instance @variable

belongs to one object (the class instance) and each object has it own

is commonly used to **store object state**




#### class @@variable

is owned and shared by the class, the instances, and the subclasses

doesn't work well with inheritance, because it can be inherited and overridden

is commonly used to store global state within the class hierarchy




## ⚠️ class variable inheritance can be tricky

```ruby
class Animal
  @@type = 'Generic'
end

class Cat < Animal
  @@type = 'Feline'
end

class Dog < Animal
  def self.type
    puts @@type
  end
end

>> Dog.type
Feline
=> nil
```




# References
- [[OOP concepts]]
- [[inheritance]]
