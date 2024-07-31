BookHaven Database Schema
Overview
This project involves designing a relational database for "BookHaven," a bookstore management system. The database manages books, authors, customers, and transactions efficiently, addressing issues like data redundancy and inconsistent data retrieval.

Tables and Columns
Authors
author_id (INT, PK): Unique identifier for each author.
name (VARCHAR(255)): Name of the author.
biography (TEXT): A brief biography of the author.
Books
book_id (INT, PK): Unique identifier for each book.
title (VARCHAR(255)): Title of the book.
author_id (INT, FK): References Authors.author_id, indicating the author of the book.
genre (VARCHAR(100)): Genre of the book.
price (DECIMAL(10, 2)): Price of the book.
publication_date (DATE): Date when the book was published.
available (BOOLEAN): Availability status of the book.
Customers
customer_id (INT, PK): Unique identifier for each customer.
name (VARCHAR(255)): Name of the customer.
email (VARCHAR(255)): Email address of the customer.
phone (VARCHAR(20)): Phone number of the customer.
Transactions
transaction_id (INT, PK): Unique identifier for each transaction.
book_id (INT, FK): References Books.book_id, indicating the book involved in the transaction.
customer_id (INT, FK): References Customers.customer_id, indicating the customer involved in the transaction.
transaction_date (DATE): Date of the transaction.
quantity (INT): Number of books involved in the transaction.
total_price (DECIMAL(10, 2)): Total price of the transaction.
Relationships
Books and Authors: A many-to-one relationship where each book is written by one author (author_id in Books references author_id in Authors).
Transactions and Books: A many-to-one relationship where each transaction involves one book (book_id in Transactions references book_id in Books).
Transactions and Customers: A many-to-one relationship where each transaction is associated with one customer (customer_id in Transactions references customer_id in Customers).
