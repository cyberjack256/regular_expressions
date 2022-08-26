### Activity One (SOLVED): Finding Credit Card Numbers With Regex

1. An analyst at our organization has provided a list of credit card numbers, parsed from a data set. We are tasked with looking for four stolen VISA credit card numbers that were used in a transaction.
How could we find those cards in this sea of numbers?

- Hint: VISA account numbers start with a “4”. According to VISA’s developer API documentation, we are looking for cards that only allow numbers with 16 digits

**Answer**: 
```regex
^[4]{1}[0-9]{15}$
```
**or**
```regex
^[4]{1}\d{15}$
```

2. What if the cards were MasterCard?

- Hint: Mastercard account numbers start with prefixes ranging from “51” to “55”, and are 16 digits in length.

**Answer**: 
```regex
^[5]{1}[1-5]{1}[0-9]{14}$
```
**or**
```regex
^[5]{1}[1-5]{1}\d{14}$
```
```text
American Express
378282246310005
American Express
371449635398431
American Express Corporate
378734493671000
Australian BankCard
5610591081018250
Diners Club
30569309025904
Diners Club
38520000023237
Discover
6011111111111117
Discover
6011000990139424
JCB
3530111333300000
JCB
3566002020360505
MasterCard
5555555555554444
MasterCard
5105105105105100
Visa
4111111111111111
4532238469013655
4929873515076297
4012888888881881
Visa (invalid)
4222222222222
44839284093824933
422222222222200054646464
2343434539867531989028393
```