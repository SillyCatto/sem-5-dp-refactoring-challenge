## Identified Code Smells
## **`ID: 220042162`**

1. Long if-else chain
   - SystermFlowRunner class has methods with long if-else chains for checking user selected operation
   -

2. Large class
   - SystemFLowRunner class has too many responsibilities
   - Invoice class has unrelated methods- `takePayment()` and `markCarAsUnavailable()`
   - DataStore manages 4 entities altogether: Invoice, Seller, Buyer, Vehicles
   -

3. Duplicate code
   - In SystemDatabase class, `findBuyerById(String id)` `findSellerById(String id)` and `findVehicleByRegistrationNumber(String registrationNumber)` methods are very similar and have duplicate code portions
   - SystemDatabase class has methods: `showInventory()`, `showBuyerList()`, `showSellerList()`, `showInvoices()` they have very similar code portions

4. Primitive obsession
   - Vehicle class uses a many primitive variables

5. Data class
   - Person, Buyer, Seller are data classes
   - Bus, Car, Hatchback, Sedan, SUV classes have only fields with getter-setters, so these are data classes as well

6. Lazy class
   - Seller class is very minimal and does too little

7. Feature envy
   - Invoice class, `markCarAsUnavailable()` method uses data of other class `ShoppingCart` more than its own data

8. Magic numbers
   - SystemFlowRunner class methods uses random magic numbers which are hard to understand at first glance

9. Long method
   - SystemFlowRunner run() method is a long method