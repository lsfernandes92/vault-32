2025-06-20 15:47

Status: #adult

Tags: [[dev]] [[oop]]

# dependency inversion/injection principle (DIP)

it says that entities should rely on abstractions and not concretions

it avoids tight coupling

❌ bad code example:
```ruby
class Printer
  def initialize
    # Here we have a tight coupling
    # relationship with the
    # HTMLParser class.
    # We also condemn our formatter
    # to be of the this type only
    @formatter = HTMLPrinter.new
  end
  
  def print(data)
    @formatter.print(data)
  end
end

class HTMLPrinter
  def print(data)
    puts "<html>#{data}</html>"
  end
end

>> printer = Printer.new
>> printer.print 'example'
<html>example</html>
=> nil
```

✅ good code example:
```ruby
class Printer
  def initialize(formatter = HTMLPrinter.new)
    @formatter = formatter
  end
  
  def print(data)
    @formatter.print(data)
  end
end

class HTMLPrinter
  def print(data)
    puts "<html>#{data}</html>"
  end
end

class JSONPrinter
  require 'json'
  
  def print(data)
    puts JSON.generate({ message: data })
  end
end

>> printer = Printer.new
>> printer.print 'example'
<html>example</html>
=> nil

>> another_printer = Printer.new(JSONPrinter.new)
>> another_printer.print 'example'
{"message":"example"}
=> nil
```




# References

- [[OOP concepts]]
- [[SOLID 101 - A Review for Rubyists - Ancient City Ruby 2016]]
