2025-06-03 12:03

Status:

Tags:

# safe swap idiom

```ruby
```ruby
def reverse_string(s)
    (s.size/2).times { |i| s[i], s[-(i+1)] = s[-(i+1)], s[i] }
    s
end
```
```
```

```ruby
def reverse_string(s)
    (s.size/2).times { |i| s[i], s[-(i+1)] = s[-(i+1)], s[i] }
    s
end
```
# References

