2025-05-28 18:08

Status: #adult 

Tags: [[dev]] [[oop]]

# polymorphism

polymorphism means **many forms**

at it's core, in ruby, it means being able to send the same message to different objects and get different results

in ruby, polymorphism is achieved through **inheritance**, **duck typing**, and through the use of **design patterns** by using the **decorator pattern**

one example of polymorphism can simplify our code:
```ruby
class Parser
  def parse(type)
    puts 'The Parser class receive the parse method'

	if type == :xml
	  puts 'An instance of the XmlParse class receive the parse message'
	elsif type == :json
	  puts 'An instance of the JsonParse class receive the parse message'
	end
  end
end
```

&&

```ruby
class Parser
  def parse(parser)
    puts 'The Parser class receive the parse method'
    parser.parse
  end
end

class XmlParser
  def parse
    puts 'An instance of the XmlParse class receive the parse message'
  end
end

class JsonParser
  def parse
    puts 'An instance of the JsonParse class receive the parse message'
  end
end
```

this example takes advantage of the polymorphism to get rid of the if branches. in this particular example it also encapsulate the parser logic on its own classes and satisfying the SRP principle




## polymorphism through inheritance

example:
```ruby
class GenericParser
  def parse
    raise NotImplementedError, 'You must implement the parse method'
  end
end


class XMLParser < GenericParser
  def parse
    puts 'An instance of the XMLParser class received the parse method'
  end
end

class JSONParser < GenericParser
  def parse
    puts 'An instance of the JSONParser class received the parse method'
  end
end
```

&&

```shell
parser = XMLParser.new
parser.parse
=> An instance of the XMLParser class received the parse method
=> nil

parser = JSONParser.new
parser.parse
=> An instance of the JSONParser class received the parse method
=> nil
```




## polymorphism through duck typing

example:
```ruby
class XMLParser
  def parse
    puts 'An instance of the XMLParser class received the parse method'
  end
end

class JSONParser
  def parse
    puts 'An instance of the JSONParser class received the parse method'
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
parser.parse(JSONParser.new)
=> An instance of the XMLParser class received the parse method
=> nil

parser.parse(XMLParser.new)
=> An instance of the JSONParser class received the parse method
=> nil

```
# References
- [[OOP concepts]]
- [[duck typing]]
- [[inheritance]]
- [Back to Basics: Polymorphism and Ruby](https://thoughtbot.com/blog/back-to-basics-polymorphism-and-ruby)
