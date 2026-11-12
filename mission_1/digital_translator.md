# Py-SECTION 1 MISSION PROJECT — THE DIGITAL TRANSLATOR

Mission: mission-03
Squad: Solo 247

**Tier 1-Basic Understanding: The Literal Assistant**
*make me a hot coffee*
1. start
2. open the heater on the table
3. hold the jug at the handle on the table and raise the jug containing water
4. Pour the water into heater 
5. stop pouring the water at 50 cl mark of the heater
6. close the heater
7. set the heater to 70 degree Celsius.
8. turn on the switch
9. Wait until elapsed time equal 3 minutes, then set switch state to OFF.
10. hold the handler and raised it 
11. tilt jug at a 45-degree angle until sensor detects 33 cl has left heater to the cup with a spoon in it on the table
12. pick the sachet of coffee on the table
13. tear top edge along perforation of the sachet of coffee.
14. open it and empty all into the cup containing the water
15. stir the spoon in the cup for 1 min
16. raise an alarm of completion, and hold the handler to hold the handle
   
**Tier 2 — Field Exercise: Algorithm Thinking**
*The ATM*
1. insert the card
2. verify the card; bank, account details and date
3. Reject card if expired or unregistered card or accredited bank or card can't be read 
4. Request PIN
5. PIN Retry Loop if pin is wrong (three attempts only)
6. Select withdrawal among bank operations
7. Enter amount
8. Check available balance
9. Reject operation when there is insufficient funds (requested amount more than available funds)
10. Cancel transaction, display error message, and return card
11. Dispense cash
12. Update account
13. return card



**Tier 3 — Practical Exercise: Input → Processing → Output**
*The Simple Calculator*

1. input two numbers
example:

number_1 = 20
number_2 = 5
2. receive the two inputs
3. check if they are integers
4. if they are not inform the user only integers allowed
5. Print a message showing the available operatios: Addition, Subtraction, Multiplication, Division
6. select addition among operations
8. add the two numbers
9. print the result

10. return back to the operations loop
11. select subtraction
12.  subtract the numbers
13. print the result

14. return back to the operations loop
15. select Multiplication
16. multiply the numbers
17. print the result

18. return back to the operations loop
19. select Division
20. check if the denominator is zero
21. request user choice to change the number or loop to operations
22. divide the numbers
23. print the result

24. return back to the operations loop
25. select exit to quit



**Tier 4 — Conceptual Challenge: Data Translator**
*Consider this customer information:*

- input user data
- Real-world information
Customer name: Victor
Age: 30
Account balance: 150000.50
Account active: Yes

- data validation; incorrect data causes the system to miscalculate balances.

- Data representation
Victor	Text
30	Number
150000.50	Number
Yes	True

- Numerical/digital representation
Victor	86 105 99 116 111 114  (Decimal)
30	30 (Decimal)
150000.50	49 53 48 48 48 48 46 53 48 (Decimal)
Yes	49

- Binary data
Victor	01010110 01101001 01100011 01110100 01101111 01110010  (Binary)
30	00011110  (Binary)
150000.50	00110001 00110101 00110000 00110000 00110000 00110000 00101110 00110101 00110000  (Binary)
Yes	00110001  (Binary)

-Stored by the computer


**Tier 5 — Architecture Challenge: Explain the Whole System**
*The Online Store*
-Customer Input
the product they want
quantity
delivery information
turn ON online location or type manually
payment information

- Application / Program

- Instructions
check the availability of product
if not available, return the user back to input form
check quantity available of the product
if not available, return the user back to input form
calculate the order total 
process the order information and show the total
select payment options
decline wrong pin or expired card or unaccredited card
return the user back to input form

- Data Processing
For example:

Product price: 50,000
Quantity: 2
------------------------
Order total: 100,000

- Stored Data
store the information in right order  
For example:

Customer
Product
Quantity
Order amount
Order status

- Result / Output
provides the total amount of order
For example:

Order confirmed. Total: 100,000.

- payment
process the payment
Check available balance
Reject operation when there is insufficient funds (requested amount more than available funds)
option to reduce orders or quantities or reduce to user input form
pay total order if order is equal to available funds
raise an alarm of successful payment

Customer
↓
Customer Input (Product, Quantity, Delivery & Payment Info)
↓
Application / Program (Instructions & Validation Checks)
↓
Data Processing (Calculating Totals & Verifying Funds)
↓
Stored Data (Saving Order & Customer Records)
↓
Result (Order Confirmation & Receipt)


Final Reflection:
A computer is not a human that understands ambiguous and contextual instructions; it is strictly literal and without intuition. It needs clear, unambiguous, and descriptive instructions to accomplish tasks, and it relies on structured digital representations of real-world information rather than understanding the real world directly.