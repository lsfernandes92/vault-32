2025-06-20 15:45

Status: #adult

Tags: [[dev]] [[oop]]

# interface segregation principle (ISP)

ruby developers tend to ignore it because of the flexibility and dynamic nature of the language

it says that we should know little as possible about other objects we're interacting

❌ good bad example we often see on long-standing rails application:
```shell
# want to know what country the user from: 
user_country = user.billing.address.country
```

✅ good example:
```shell
user_country = user.country
```




# References

- [[OOP concepts]]
- [[SOLID 101 - A Review for Rubyists - Ancient City Ruby 2016]]
