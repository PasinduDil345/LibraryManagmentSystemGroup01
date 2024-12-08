# Library Management System

## Overview
The **Library Management System** is designed to streamline library operations, including book inventory management, member registration, staff assistance, and loan transactions. The system supports core functionalities such as issuing and returning books, maintaining member records, and managing library staff.

## Components

### 1. Library
- **Attributes**:
  - `List of books`: Maintains all books in the library's inventory.
  - `List of members`: Records all registered library members.
  - `List of Staff`: Records all library staff.
- **Methods**:
  - `addBook(Book)`: Adds a new book to the library's inventory.
  - `removeBook(Book)`: Removes a book from the inventory.
  - `registerMember(LibraryMember)`: Registers a new library member.
  - `removeMember(LibraryMember)`: Remove a library member.

---

### 2. Book
- **Attributes**:
  - `isbn (String)`: Unique identifier for the book.
  - `title (String)`: Title of the book.
  - `author (String)`: Author of the book.
  - `status (String)`: Availability status of the book (e.g., Available, Borrowed).
  - `publicationYear (int)`: Year the book was published.
- **Methods**:
  - `getInfo()`: Retrieves detailed information about the book.

---

### 3. Library Member
- **Attributes**:
  - `List of borrowed books`: Keeps track of books borrowed by the member.
- **Methods**:
  - `borrowBook(Book, int): LoanTransaction`: Initiates the borrowing process by creating a loan transaction.
  - `returnBook(LoanTransaction)`: Processes the return of a borrowed book.

---

### 4. Loan Transaction
- **Attributes**:
  - `transactionId (String)`: Unique identifier for the loan transaction.
  - `member (LibraryMember)`: The library member involved in the transaction.
  - `book (Book)`: The book being borrowed or returned.
  - `borrowedDate (Date)`: The date the book was borrowed.
  - `dueDate (Date)`: The due date for returning the book.
- **Methods**:
  - `completeTransaction()`: Marks the loan transaction as complete.

---

### 5. Librarian
- **Attributes**:
  - `name (String)`: The librarian's name.
  - `id (String)`: The librarian's unique ID.
  - `contactInfo (String)`: Contact details of the librarian.
- **Methods**:
  - `receiveBook(LoanTransaction)`: Processes the return of a book.
  - `issueBook(LoanTransaction)`: Issues a book to a library member.
  - `getDetails()`: Retrieves the librarian's information.

---

### 6. Staff
- **Attributes**:
  - `employeeId (String)`: Staff member's unique ID.
  - `position (String)`: Staff member's position in the library.
- **Methods**:
  - `manageInventory()`: Manages the library's inventory.
  - `assistMember(LibraryMember)`: Assists library members with their queries or issues.

---

## Relationships

- **Library and Librarian**: A library employs one or more librarians to manage operations.
- **Library and Library Member**: Members register with the library and can borrow books.
- **Library Member and Loan Transaction**: Members can perform multiple loan transactions.
- **Loan Transaction and Book**: Each transaction involves issuing or returning a specific book.
- **Librarian and Loan Transaction**: Librarians facilitate book issue and return transactions.

---

## Usage

### Adding Books
- Librarians or staff can add books to the inventory using the `addBook()` function.

### Registering Members
- Library members are registered using the `registerMember()` function.

### Issuing and Returning Books
- Members borrow books by creating a loan transaction (`borrowBook()`).
- The transaction is marked complete when the book is returned (`returnBook()`).

### Managing Inventory
- Staff members manage the library's inventory using the `manageInventory()` method and assist library members with their needs.

---

## Contributors
- **Group Number**: [Group 01]
- **Team Members**:
  1. 22UG1-0390_K.P.Dilhara
  2. 22ug1-0936_Bangamuwage C.A.H.
  3. 22ug1-0471_K.K.Pahan Bimsara
  4. 22ug1-0082_H.V.Rashini Nilumika
  5. 22ug1-0753_T.R.A.Dinesh Rodriguez
  6. 22ug1-0923_S.Piranavan
  7. 22ug1-0480_H.A.L.Ruwanya

---

