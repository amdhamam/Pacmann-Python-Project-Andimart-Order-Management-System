# Andimart Kebayoran - Order Management System

This Python script provides a simple console-based order management system for Andi Supermart Kebayoran. It allows customers to add items to their order, update item details, delete items, and checkout. The system also includes features for calculating discounts, validating phone numbers, and generating unique transaction IDs.

## Features

- **Add items to the order**: Users can add items to their order by specifying the item name, quantity, and price.

- **Update item details**: Users can update the name, quantity, and price of items in their order.

- **Delete items from the order**: Users can remove items from their order.

- **Reset the order**: Users can clear all items from their order.

- **Update customer details**: Users can update their customer details, including their name, order type, phone number, and order date.

- **Check order details**: Users can view their current order details, including a list of all items in the order and the grand total.

- **Checkout**: Users can checkout their order, which includes selecting a payment method and confirming the order. The system will then calculate any applicable discounts and print a receipt.

## Usage

1. Run the script in your Python environment.
2. Follow the prompts to add items to your order, update customer details, and checkout.

## Code Overview

The script includes several functions to manage the order and customer details:

- `validate_phone_number(phone_number)`: Validates the phone number input. It uses a regular expression to ensure that the phone number is between 10 and 15 digits long.

- `transaction()`: Creates a unique transaction ID. This ID is a combination of a random number between 100 and 999 and the string 'trnsct_'.

- `print_order()`: Prints the customer details and current order status. It uses the PrettyTable library to format the order details in a table.

- `update_customer_details()`: Updates the customer details. It prompts the user to enter their name, order type, phone number, and order date. It also validates the phone number and generates a unique customer ID.

- `update_item_name()`, `update_item_price()`, `update_item_qty()`: These functions update the name, price, and quantity of an item in the order. They prompt the user to enter the index of the item they want to update and the new value.

- `delete_item()`: Deletes an item from the order. It prompts the user to enter the index of the item they want to delete.

- `reset_transaction()`: Resets the order. It clears all items from the order.

- `add_item()`: Adds an item to the order. It prompts the user to enter the item name, quantity, and price, and then adds the item to the order.

- `check_order_details()`: Prints the order details. If there are no items in the order, it prints a message saying that the cart is empty.

- `calculate_discount(grand_total)`: Calculates the discount based on the grand total. It applies a discount rate of 7% for orders over 500,000, 6% for orders over 300,000, and 5% for orders over 200,000.

- `get_payment_method()`: Prompts the user to select a payment method from a list of available methods.

- `select_payment_method()`: Selects a payment method. It prompts the user to enter their selection and updates the global payment_method variable.

- `print_receipt()`: Prints the receipt. It prints the customer details, order details, grand total, discount,

total after discount, and payment method. It also calls the `checkout()` function to finalize the order.

- `checkout()`: Checks out the order. It first calls the `select_payment_method()` function to select a payment method. Then, it calculates the grand total, discount, and total after discount. It prints these details along with the customer details and order details. Finally, it prompts the user to confirm the order. If the user confirms the order, it prints a success message and clears the order. If the user does not confirm the order, it prints a message saying that the order has not been placed.

## Database

The script uses SQLite to manage the transactions. It creates a connection to a SQLite database file named 'transactions.db'. The database is used to store the transaction details, including the customer details, order details, and payment method.

## Flowchart

![Flowchart Diagram](https://github.com/amdhamam/Pacmann_Andimart/blob/main/Flowchart%20Diagram.png?raw=true "Flowchart Diagram")


## Dependencies

The script uses the following Python libraries:

- `time`: Used to generate timestamps for the transactions.
- `random`: Used to generate random numbers for the transaction IDs.
- `datetime`: Used to handle dates for the orders.
- `sqlite3`: Used to manage the SQLite database.
- `prettytable`: Used to format the order details in a table.
- `re`: Used to validate the phone number input using a regular expression.

## Setup

To run the script, you need to have Python installed on your machine. You also need to install the `prettytable` library, which can be installed via pip:

```bash
pip install prettytable
```

After installing the necessary dependencies, you can run the script using Python:

```bash
andimart order_management.py
```

This will start the order management system and prompt you to enter your customer details and order details.

## Future Improvements

- Implement a user authentication system to allow customers to log in and view their past orders.
- Add support for multiple order types, such as dine-in, take-out, and delivery.
- Improve the database schema to better organize the transaction data.
- Add error handling to ensure that the script can recover from unexpected inputs or database errors.
- Implement a graphical user interface (GUI) to make the system more user-friendly.
```

This README.md file provides a more detailed overview of the script, including a description of each function, the database, the dependencies, how to set up and run the script, and potential future improvements.
