#### Expense Tracker
This project is a simple Expense Tracker implemented in Python using Object-Oriented Programming (OOP). It consists of two main classes:

Expense: Represents an individual financial expense with attributes like id, title, amount, created_at, and updated_at.
ExpenseDatabase: Manages a collection of expenses, allowing adding, removing, and retrieving expenses by ID or title.



#### `update(self, title: str = None, amount: float = None)`
- Updates the expense details.
- If `title` is provided, updates `self.title`.
- If `amount` is provided, updates `self.amount`.
- `self.updated_at = datetime.utcnow()`: Updates the modification timestamp.

#### `to_dict(self)`
- Converts the `Expense` object into a dictionary.
- Returns a dictionary with `id`, `title`, `amount`, `created_at`, and `updated_at` in ISO format.

### `ExpenseDatabase` Class
#### `__init__(self)`
- Initializes an empty list `self.expenses` to store expense objects.

#### `add_expense(self, expense: Expense)`
- Adds an `Expense` instance to `self.expenses` list.

#### `remove_expense(self, expense_id: str)`
- Removes an expense by filtering out the one with the given ID.

#### `get_expense_by_id(self, expense_id: str)`
- Iterates through `self.expenses` to find an expense with the given ID.
- Returns the expense if found, otherwise returns `None`.

#### `get_expense_by_title(self, title: str)`
- Returns a list of expenses that match the given title (case insensitive).

#### `to_dict(self)`
- Converts all stored expenses into a list of dictionaries by calling `to_dict()` on each `Expense` instance.

### Example Usage
- Creates an instance of `ExpenseDatabase`.
- Adds two expenses (`Groceries` and `Transport`).
- Prints all stored expenses in a structured dictionary format.



## How to Clone the Repository
To clone this repository, use the following command:

```sh
git clone <repository-url>
```

Replace `<repository-url>` with the actual URL of the GitHub repository.

## How to Run the Code
After cloning the repository, navigate into the project directory:

```sh
cd expense-tracker
```

Then, run the script using Python:

```sh
python expense_tracker.py
```

This will execute the example usage provided in the script and display the list of expenses in JSON format.
