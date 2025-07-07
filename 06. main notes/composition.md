2025-05-30 11:15

Status: #adult

Tags: [[oop]] [[dev]] [[ruby]]

# composition

composition means **building complex behavior by combining smaller objects**, rather than using class inheritance

with composition you **delegate behavior to other objects**

code example:
```ruby
class Engine
  def start
    puts "Engine is starting..."
    puts "Engine has started!"
  end
end

class Vehicle
  def initialize
    @engine = Engine.new
  end

  def start
    @engine.start
  end
end
```


# References
- [[OOP concepts]]
- [[composition vs inheritance]]
- [[inheritance]]