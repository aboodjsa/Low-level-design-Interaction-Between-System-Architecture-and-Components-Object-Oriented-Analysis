# Object-Oriented Analysis

# Main Classes

## Book
Attributes:
- book_id
- title
- author
- isbn
- available

Methods:
- issue_book()
- return_book()

---

## Member
Attributes:
- member_id
- name
- borrowed_books

Methods:
- can_borrow()

---

## Librarian
Attributes:
- librarian_id
- name

---

## Transaction
Attributes:
- issue_date
- return_date

Methods:
- calculate_fine()

---

# Class Diagram

```mermaid
classDiagram

class Book{
+book_id
+title
+author
+isbn
+available
+issue_book()
+return_book()
}

class Member{
+member_id
+name
+borrowed_books
+can_borrow()
}

class Librarian{
+librarian_id
+name
}

class Transaction{
+issue_date
+return_date
+calculate_fine()
}

Member --> Transaction
Book --> Transaction
Librarian --> Transaction
```

---

# Use Case Diagram

```mermaid
flowchart LR

Member((Member))
Librarian((Librarian))

UC1[Search Book]
UC2[Borrow Book]
UC3[Return Book]
UC4[Add Book]

Member --> UC1
Member --> UC2
Member --> UC3

Librarian --> UC4
```

---

# Sequence Diagram — Issue Book

```mermaid
sequenceDiagram

Librarian->>System: Issue Book
System->>Book: Check availability
Book-->>System: Available
System->>Transaction: Create transaction
System-->>Librarian: Success
```

---

# State Diagram — Book Lifecycle

```mermaid
stateDiagram-v2

[*] --> Available
Available --> Issued
Issued --> Returned
Returned --> Available
```