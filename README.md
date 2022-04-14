## Description of the problem

AllotMe has started selling herbs online:

```
+--------------|----------------|---------+
| Product Code |     Name       |  Price  |
+--------------|----------------|---------+
|     BAS      |   Basil        |  £3.11  |
|     PAR      |   Parsley      |  £5.00  |
|     COR      |   Coriander    | £11.23  |
+--------------|----------------|---------+
```

Our CEO is a big fan of buy-one-get-one-free offers and of Basil. He wants us to add a rule to do this.

The COO, though, likes low prices and wants people buying Parsley to get a price discount for bulk purchases. If you buy 3 or more Parsley, the price should drop to £4.50. Our customers can add items in any order, and because the CEO and COO change their minds often, it needs to be flexible regarding our pricing rules.

The interface to our checkout looks like this (shown in Ruby):

```
ba = Basket.new(pricing_rules)
ba.add(item)
ba.add(item)
price = ba.total
```

Implement a checkout system that fulfills these requirements in Ruby.

Here is some test data:

```
Basket items: BAS, PAR, BAS, COR
Total price expected: £19.34
```

```
Basket items: BAS, BAS
Total price expected: £3.11
```

```
Basket items: PAR, PAR, BAS, PAR
Total price expected: £16.61
```
