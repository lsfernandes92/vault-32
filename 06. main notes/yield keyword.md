2025-06-05 19:57

Status: #adult 

Tags: [[dev]] [[ruby]]

# what's the yield keyword

in ruby, yield is keyword that calls/tells the block/function that is passed to a method without explicitly naming the block as 

in ruby, yield is keyword that call a block/function that is passed to a method implicitly

code example:
```ruby
def map(array)
  new_array = []
  array.each { |elem| new_array << yield(elem) }
  new_array
end

>> map([1, 2, 3]) { |number| number * 2}
=> [2, 4, 6]
```

# References

