 # Implementation

## models.py

Contains:
- Book class
- Member class
- Librarian class
- Transaction class

---

## library_system.py

Contains:
- BookCatalog
- LibraryService

Handles:
- issuing books
- returning books
- searching books

---

## main.py

Demonstrates:
- adding books
- registering members
- borrowing books
- returning books

---

# Example Code

```python
book1 = Book(
    1,
    "Python Basics",
    "John Doe",
    "ISBN001",
    "Programming"
)
```

---

# Design Principles Used

## Encapsulation
Each class controls its own data.

## Abstraction
Complex operations are hidden behind methods.

## Single Responsibility Principle
Each class has one responsibility.