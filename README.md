# 📱 Mobile Shop CRUD Project

A simple command-line **Mobile Shop Management System** built in Python. It demonstrates the four core **CRUD** operations — Create, Read, Update, Delete — using a plain Python list as the in-memory data store.

## Features

- ➕ **Add Mobile** – Add a new mobile record with ID, brand, model, price, and quantity
- 📋 **Display All Mobiles** – View all mobiles in a neatly formatted table
- 🔍 **Search Mobile** – Look up a mobile by its ID
- ✏️ **Update Mobile** – Edit the details of an existing mobile
- 🗑️ **Delete Mobile** – Remove a mobile record (with confirmation)
- 🚪 **Exit** – Quit the application

## Requirements

- Python **3.10+** (uses `match-case`, introduced in 3.10)

No external libraries are required — the project uses only the Python standard library.

## Getting Started

1. Clone or download this repository.
2. Run the script:

   ```bash
   python mobile_shop.py
   ```

3. Use the on-screen menu to manage mobile records.

## How It Works

Each mobile is stored as a simple list:

```python
[id, brand, model, price, quantity]
```

**Example:**

```python
[101, "Samsung", "Galaxy A55", 35000, 5]
```

All records are kept together in a single list:

```python
mobiles = [
    [101, "Samsung", "Galaxy A55", 35000, 5],
    [102, "Apple", "iPhone 15", 65000, 3],
    [103, "OnePlus", "Nord 4", 30000, 7],
]
```

| Index | Field    | Example      |
|-------|----------|--------------|
| 0     | ID       | `101`        |
| 1     | Brand    | `"Samsung"`  |
| 2     | Model    | `"Galaxy A55"` |
| 3     | Price    | `35000`      |
| 4     | Quantity | `5`          |

## CRUD Mapping

| Operation | Function             | List Operation Used |
|-----------|-----------------------|----------------------|
| Create    | `add_mobile()`         | `append()`           |
| Read      | `display_mobiles()`    | `for` loop            |
| Read/Search | `search_mobile()`    | `for` loop + condition |
| Update    | `update_mobile()`      | Modify list elements  |
| Delete    | `delete_mobile()`      | `remove()`            |

## Project Structure

```
mobile_shop.py   # Complete CRUD application (single file)
README.md        # Project documentation
```

## Sample Menu

```
=============================================
        MOBILE SHOP MANAGEMENT
=============================================
1. Add Mobile
2. Display All Mobiles
3. Search Mobile
4. Update Mobile
5. Delete Mobile
6. Exit
=============================================
Enter your choice:
```

## Notes / Limitations

- Data is stored **in memory only** — all records are lost when the program exits (no file or database persistence).
- Mobile IDs must be unique; `add_mobile()` checks for duplicates before inserting.
- Input validation is minimal — entering non-numeric values for ID, price, or quantity will raise an error.

## Possible Improvements

- Persist data to a file (CSV/JSON) or a database (SQLite)
- Add input validation and error handling (`try/except`)
- Support sorting/filtering (e.g., by brand or price range)
- Add unit tests for each CRUD function

## License

This project is free to use for learning and educational purposes.