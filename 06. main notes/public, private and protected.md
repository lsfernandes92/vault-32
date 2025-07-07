2025-06-05 16:41

Status: #adult

Tags: [[dev]] [[ruby]]

# `public`, `private` and `protected` in ruby

they are method visibility keywords that control **who** and **where** the method can be called

they **enforce encapsulation** and **define boundaries between objects**




## firstly, what is an explicit receiver?

it's an object that is explicit receiving the method call

example:
```ruby
=> user = User.new

# here the variable `user`
# is an explicit receiver
=> user.full_address
```




## public

default visibility for methods

can be accessed from inside and outside the class

allows explicit receiver



## private

can be accessed from inside the class only

don't allow explicit receiver, even `self`



## protected

can be called within the same class or its subclasses, and between instances of the same class(but still within the same class)

allows explicit receiver only within the same class

example:
```ruby
class Person
  def initialize(age)
    @age = age
  end

  # here is the explicit receiver
  # within the same class
  def older_than?(other_person)
    self.what_my_age_again > other_person.what_my_age_again 
  end

  protected

  def what_my_age_again
    @age
  end
end

>> lucas = Person.new(32)
>> maya = Person.new(35)
>> lucas.older_than?(maya)
=> true

# and here is the explicit receiver
# been called outside the class
>> maya.age
=> protected method `what_my_age_again' called for #<Person:0x000000010500cd68 @age=35> (NoMethodError)

```




# References

