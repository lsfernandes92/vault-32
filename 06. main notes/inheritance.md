2025-05-28 17:48

Status: #adult 

Tags: [[dev]] [[oop]]

# inheritance

it's used to share behavior between classes

it's when a child class inherits attributes and methods from a parent class

promotes code reuse

**avoid** inheritance if you only want to share behavior

ruby only supports single inheritance

use **super** to call the parent class equivalent method. example:
```ruby
class Animal
  def initialize(name)
    @name = name
  end

  def speak
    "#{@name} makes a sound."
  end
end

class Dog < Animal
  def initialize(name)
    super(name)
  end

  def speak
    "#{super} Woff!"
  end
end
```


ruby uses method lookup chain. it first checks the object class, then it checks the super class, then continues up the chain until it reaches `BasicObject`

rails use it heavily with, for example, `UserController < ApplicationController` and `ApplicationController < ActionController::Base`

# References
- [[OOP concepts]]
- [[composition]]
- [[composition vs inheritance]]
