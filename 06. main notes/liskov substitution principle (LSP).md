2025-06-20 15:42

Status: #adult

Tags: [[dev]] [[oop]]

# liskov substitution principle (LSP)

it says that if we substitute our parent class with any subclasses, it should work properly as if we were passing the parent class

as long as the object are in the same relationship context (of this whole ideia of "how am I interacting with this object"), then I should be able to swap in different subtypes/subclasses

relationship context:
different types of frisbee disks are in the same context of flying objects/playing frisbee, but not in the context of, for example, things to put over your head

❌ bad code example:
```ruby
class Player
  def initialize(name)
    @name = name
  end

  def preferred_position
    nil
  end
end

class PlayerOne < Player
  def initialize(name)
    super(name)
  end

  def preferred_position
    'damage'
  end
end

class PlayerTwo < Player
  def initialize(name)
    super(name)
  end

  # Liskov arguments that we must have
  # consistency between parent class
  # and subclasses
  def preferred_position
    { position: 'support' }
  end
end
```




# References

- [[OOP concepts]]
- [[SOLID 101 - A Review for Rubyists - Ancient City Ruby 2016]]
