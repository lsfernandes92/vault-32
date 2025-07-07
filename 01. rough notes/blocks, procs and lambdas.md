2025-06-05 17:46

Status: #adult #wip

Tags: [[dev]] [[ruby]]

# blocks, procs and lambdas

ruby uses multi paradigms of programming, mostly object oriented and functional

blocks, procs and lambdas are all anonymous functions



## what are anonymous functions?

in javascript the only difference is that anonymous function is not named

example:
```javascript
// anonymous arrow function
>> const anonymousAdder = (a, b) => { return a + b; }
>> anonymousAdder(1, 2)
=> 3

>> function adder (a, b) { return a + b; }
>> adder(1, 2)
=> 3
```

in ruby we don't have that idea as much as we do with methods or with **stabby lambda**

example:
```ruby
>> def adder(num1, num2) = num1 + num2
>> adder(1, 2)
=> 3

>> adder = -> (num1, num2) { num1, num2 }
>> adder.call(1, 2)
>> adder.(1, 2)
>> adder[1, 2]
=> 3 
```




## all method arguments are valid as function arguments

```ruby
def all_valid_args(a, b = 1, *cs, d:, e: 2, **fs, &fn); end

# this is one thing you can do
lambda_multiply = -> array, &fn {
  new_list = []
  array.each { |elem| new_list << fn.call(elem) }
  new_list
}

>> lambda_multiply.call([1, 2]) { |value| value * 2 }
=> [2, 4]
```




## where function are used in ruby?

they're used everywhere

when we use `each`, for example, that's a block function




## ampersand (&) and `to_proc`

the ampersand tells ruby to turn what's after it into a proc by calling the method `Symbol#to_proc`

```ruby
# it calls the event method
# on every element and it
# only works on this context
>>[1, 2, 3].select(&:even?)
=> [2]

# it effectively generates
>> [1, 2, 3].select { |number| number.even? }
=> [2]
```




## types of functions

there three types: block functions, proc functions and lambda functions

#### block functions

are the most common to see in a ruby code. the `each` method is one example of that

there are two ways of pass/call a block function in a method. explicit or implicit

example:
```ruby
# the explicit way
def map(array, &block)
  new_array = []
  array.each { |elem| new_array << block.call(elem) }
  new_array
end

>> map([1, 2, 3]) { |number| number * 2 }
=> [2, 4, 6]

# the implicti way
# using yield keyword
def map(array)
  new_array = []
  array.each { |elem| new_array << yield(elem) }
  new_array
end

>> map([1, 2, 3]) { |number| number * 2}
=> [2, 4, 6]
```




## how to avoid missing block?

use built in method `block_given` to guard clause if a block is not given

example:
```ruby
def map(array, &block)
  return 'no block given' unless block_given?

  new_array = []
  array.each { |elem| new_array << block.call(elem) }
  new_array
end

>> map([1, 2, 3])
=> "no block given"
```
# References
- [# Understanding Ruby - Blocks, Procs, and Lambdas](https://dev.to/baweaver/understanding-ruby-blocks-procs-and-lambdas-24o0)
