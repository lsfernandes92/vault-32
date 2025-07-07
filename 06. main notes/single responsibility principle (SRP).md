2025-06-20 15:31

Status: #adult 

Tags: [[dev]] [[oop]]

# single responsibility principle (SRP)

class should have only one reason to change

class should do only one thing

we don't want our software to break and that can happen if we don't organize well our objects responsibilities. active record objects are one example of this

❌ bad code example:
```ruby
class User
  attr_reader :name, :email
  
  def initialize(name, email)
    @name = name
    @email = email
  end

  def save_to_file
    # code to manage and persist I/O files 
  end
end
```

✅ good code example:
```ruby
class User
  attr_reader :name, :email
  
  def initialize(name, email)
    @name = name
    @email = email
  end
end

class UserFileWriter
  def save_to_file(user)
    # code to manage and persist I/O files 
  end
end
```




# References

- [[OOP concepts]]
- [[SOLID 101 - A Review for Rubyists - Ancient City Ruby 2016]]
