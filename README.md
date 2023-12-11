# Budget App

Welcome to the FreeCodeCamp Budget App challenge! In this project, we'll be working on the `Category` class in `budget.py`. The `Category` class is responsible for managing budget categories such as food, clothing, and entertainment. It includes various methods to handle deposits, withdrawals, transfers, and checking funds.

## Category Class

### Methods

- **`__init__(self, category)`**: Initializes the category with a given name. Sets up an instance variable called `ledger` as an empty list.

- **`deposit(self, amount, description="")`**: Deposits the given amount with an optional description. Appends an object to the `ledger` list in the form of {"amount": amount, "description": description}.

- **`withdraw(self, amount, description="")`**: Withdraws the given amount with an optional description. If there are not enough funds, nothing is added to the ledger. Returns True if the withdrawal took place, and False otherwise.

- **`get_balance(self)`**: Returns the current balance of the budget category based on deposits and withdrawals.

- **`transfer(self, amount, budget_category)`**: Transfers the given amount to another budget category. Updates both ledgers with withdrawal and deposit entries. Returns True if the transfer took place, and False otherwise.

- **`check_funds(self, amount)`**: Checks if the given amount is greater than the balance of the budget category. Returns False if the amount is greater than the balance and True otherwise. Used by both the `withdraw` and `transfer` methods.

- **`__str__(self)`**: Returns a formatted string when the budget object is printed. Includes a title line, a list of items in the ledger, and a line displaying the category total.

### Example

```python
food_category = Category("Food")
food_category.deposit(1000, "initial deposit")
food_category.withdraw(10.15, "groceries")
food_category.withdraw(15.89, "restaurant and more food")
food_category.transfer(50, "Clothing")

print(food_category)
