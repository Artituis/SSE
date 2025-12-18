# Use Case Structure

### Use Case Name: Process Sale
### Actor: Cashier
### Precondition: Customer arrives at a POS checkout with the items to purchase
### Postcondition: 
Sale is saved. Receipt is printed. Stock data updated. Payment
authorization approvals are recorded
### Main Flows: Single column paragraph, bullet or numbering style format
    1. Cashier starts a new sale
    2. Cashier enters item identifier
    . . .
    5. System calculates and presents total price
    6. Customer pays and System handles payment
    . . .
    9. Customer leaves with receipt and goods.

OR

    (A customer arrives at a checkout with items to purchase. The cashier uses
    the POS system to record each purchased item. The system presents a
    running total and line-item details. The customer enters payment
    information, which the system validates and records. The system updates
    inventory. The customer receives a receipt from the system and then
    leaves with the items.)
### Alternate Flows:

2a. Invalid identifier: System signals error and rejects entry

2b. There are multiple of same item: Cashier can enter item category
identifier and the quantity

### Extension Point:

5a. Process Gift Coupon Sale UC

### Variations:
6a. Paying by cash: (UC Handle Cash Payment)
6b. Paying by credit: (UC Handle Credit Payment)