# System Architecture

## Architecture Style

The system uses a 3-tier layered architecture:

1. Presentation Layer
2. Business Logic Layer
3. Data Layer

---

# Components

## Presentation Layer
Handles user interaction.

Examples:
- Search screens
- Borrow forms
- Return forms

---

## Business Logic Layer
Processes application rules.

Examples:
- Fine calculation
- Borrow validation
- Availability checking

---

## Data Layer
Stores books, members, and transactions.

---

# Architecture Diagram

```mermaid
flowchart TD

A[User Interface]
--> B[Business Logic Layer]

B --> C[Book Service]
B --> D[Member Service]
B --> E[Transaction Service]

C --> F[(Database)]
D --> F
E --> F
```