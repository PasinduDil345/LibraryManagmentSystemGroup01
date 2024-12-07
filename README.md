Library Management System

Overview

The Library Management System is designed to manage the operations and resources of a library, including book inventory, memberships, staff, and loan transactions. The system supports key functionalities like issuing and returning books, maintaining member records, and managing library staff.

Components

1. Library
   
Attributes:
List of books
List of members

Methods:
addBook(Book): Adds a new book to the library's inventory.
removeBook(Book): Removes a book from the inventory.
registerMember(LibraryMember): Registers a new library member.

2. Book
   
Attributes:
isbn (String): Unique identifier for the book.
title (String): Title of the book.
author (String): Author of the book.
status (String): Availability status of the book.
publicationYear (int): Year of publication.

Methods:
getInfo(): Retrieves information about the book.

3. Library Member
   
Attributes:
List of borrowed books.

Methods:
borrowBook(Book, int): LoanTransaction: Initiates the borrowing process.
returnBook(LoanTransaction): Returns a borrowed book.

4. Loan Transaction
   
Attributes:
transactionId (String): Unique identifier for the transaction.
member (LibraryMember): The member involved in the transaction.
book (Book): The book being borrowed or returned.
borrowedDate (Date): The date the book was borrowed.
dueDate (Date): The due date for returning the book.

Methods:
completeTransaction(): Marks the transaction as complete.

5. Librarian
   
Attributes:

name (String): Librarian's name.
id (String): Librarian's ID.
contactInfo (String): Contact information.

Methods:

receiveBook(LoanTransaction): Processes the return of a book.
issueBook(LoanTransaction): Issues a book to a library member.
getDetails(): Retrieves the librarian's details.

6. Staff
   
Attributes:

employeeId (String): Staff member's ID.
position (String): Staff member's position.

Methods:

manageInventory(): Manages the library's inventory.
assistMember(LibraryMember): Assists library members.

Relationships

Library and Librarian:
The library employs one or more librarians who manage library operations.

Library and Library Member:
Members register with the library and can borrow books.

Library Member and Loan Transaction:
Members can perform one or more loan transactions.

Loan Transaction and Book:
A transaction involves issuing or returning a specific book.

Librarian and Loan Transaction:
Librarians facilitate loan transactions.

Usage

Adding Books:
The librarian or staff can add books to the library's inventory.

Registering Members:
Members are registered through the registerMember() function.

Issuing and Returning Books:
Members borrow books by initiating a loan transaction.
The transaction is completed when the book is returned.

Managing Inventory:
Staff manage the library's inventory and assist members.
