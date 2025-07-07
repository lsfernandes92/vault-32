2025-05-29 19:56

Status: #adult 

Tags: [[oop]] [[ruby]] [[dev]]

# duck typing

ruby doesn't care what object is, it only cares if it responds to the method you're calling

"if it walk like a duck, if it quack like a duck, then it's a duck"

example of duck typing:
```ruby
class XMLParser
  def parse
    puts 'An instance of the XMLParser class received the parse message'
  end
end

class JSONParser
  def parse
    puts 'An instance of the JSONParser class received the parse message'
  end
end

class GenericParser
  def parse(parser)
    parser.parse
  end
end
```

&& 

```shell
parser = GenericParser.new

puts 'Using XMLParser'
parser.parse(XmlParser.new)
=> Using XMLParser
=> An instance of the XmlParser class received the parse message
=> nil

puts 'Using JSONParser'
parser.parse(JsonParser.new)
=> Using JSONParser
=> An instance of the JSONParser class received the parse message
=> nil
```

&&

```bash
Using XmlParser
An instance of the XmlParser class received the parse message

Using JsonParser
An instance of the JsonParser class received the parse message
```


# References
- [[OOP concepts]]
- [[polymorphism]]
