# Greasyfork Script Links
### [Cart Page Conversion Script](https://greasyfork.org/en/scripts/463216-pandabuy-cart-conversion-prices)
### [Product Page Conversion Script](https://greasyfork.org/en/scripts/463217-pandabuy-product-price-conversion)
### [Search Page Conversion Script](https://greasyfork.org/en/scripts/463218-pandabuy-search-price-conversion)
### [Shipping Estimate Page Conversion Script](https://greasyfork.org/en/scripts/463219-pandabuy-shipping-conversion-prices)

# To change your conversion please change this singular line

#### If I wanted to go from aud to cad I would do
```diff
- const EXCHANGE_DATA = EXCHANGE_RATES["AUD"]
+ const EXCHANGE_DATA = EXCHANGE_RATES["CAD"]
```

#### If you want to addon more currencys please just do these steps
- Add a comma to the end of exchange rate bracket which looks like
```diff
const EXCHANGE_RATES = {
    "AUD": ["$", 4.66, "AUD"],
    "USD": ["", 6.89, "USD"],
+   "CAD": ["", 5.11, "CAD"],
-   "CAD': ["", 5.11, "CAD"]
}
```
- Use this template to put in your own currency
```
"SHORTENED NAME": ["CURRENCY SYMBOL", "CONVERSION RATE WITH CHIENSE YUAN", "SHORTENED NAME"]
```
- So if I wanted to add GBP it would look like
```
"GBP": ["£", 8.58, "GBP"]
```
- Now you just slot it in the end like this
```diff
const EXCHANGE_RATES = {
    "AUD": ["$", 4.66, "AUD"],
    "USD": ["", 6.89, "USD"],
    "CAD": ["", 5.11, "CAD"],
+   "GBP": ["£", 8.58, "GBP"]
}
```

# Frequently asked questions
- How would I get the conversion rate for my currency?
  - Go to GOOGLE and search up `CURRENCY_NAME to YUAN`
  - Put the digit 1 in your currency
  - Whatever number is in the "Chinese Yuan" column is the exchange rate.
  - Should look something like this

![image](https://user-images.githubusercontent.com/94208670/229727762-3bf60020-d076-4806-b095-a845ad17b2c7.png)


