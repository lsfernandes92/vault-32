2025-06-20 15:33

Status: #adult

Tags: [[dev]] [[oop]]

# open-closed principle (OCP)

class should be open for extension and closed for modification

you don't want to change existing code instead you want to reference new objects that does the new thing

❌ bad code example:
```ruby
# Let's say we're in a scenario
# where a Paypal payment method
# need to be implemented.
class PaymentProcessor
	def process(payment_type)
		case payment_type
		when :paypal
			puts 'The payment is been processed by Paypal'
		when :credit_card
			puts 'The payment is been processed by the CreditCard holder'
		else
			puts 'The payment is been paid by physical money'
		end
	end
end
```

✅ good code example:
```ruby
class PaypalPayment
  def process
    puts 'The payment is been processed by Paypal'
  end
end

class CreditCarPayment
  def process
    puts 'The payment is been processed by the CreditCard holder'
  end
end

class PaymentProcessor
  def process(payment_method)
    payment_method.process
  end
end
```




# References

- [[OOP concepts]]
- [[SOLID 101 - A Review for Rubyists - Ancient City Ruby 2016]]