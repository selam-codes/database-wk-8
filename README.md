# E-commerce Database Schema

### This repository contains the SQL script for a relational database designed for a simple e-commerce platform. The schema is built to manage essential entities: Customers, Products, and Orders.

## Database Structure

### The database is composed of four main tables:

#### Customers: Stores user information.

#### CustomerID (Primary Key)

#### Email (Unique, Not Null)

#### RegistrationDate

#### Products: Holds product details.

#### ProductID (Primary Key)

#### ProductName (Unique, Not Null)

#### Price (Not Null, > 0)

#### StockQuantity (Not Null, >= 0)

#### Orders: Logs customer transactions.

#### OrderID (Primary Key)

#### CustomerID (Foreign Key)

#### OrderDate

#### TotalAmount

#### OrderItems: A junction table linking orders and products to manage the many-to-many relationship.

#### OrderItemID (Primary Key)

#### OrderID (Foreign Key)

#### ProductID (Foreign Key)

#### Quantity (Not Null, > 0)

#### PriceAtOrder

## Constraints and Relationships

#### Primary Keys: Uniquely identify each record.

#### Foreign Keys: Link tables together, establishing relationships.

#### Orders.CustomerID references Customers.CustomerID.

#### OrderItems.OrderID references Orders.OrderID.

#### OrderItems.ProductID references Products.ProductID.

#### Unique Constraints: Prevent duplicate entries for columns like Email and ProductName.

#### Check Constraints: Ensure data integrity, for example, Price and StockQuantity cannot be negative.

## Setup and Usage

#### Open MySQL Client: Use any MySQL client, such as MySQL Shell or MySQL Workbench.

#### Run the SQL Script: Execute the provided .sql file to create the database and tables.
