# sql-heladeria
# 🍦 Ice Cream Shop Management Database

## Project Description

The Ice Cream Shop Management Database is a relational database designed to manage the daily operations of an ice cream store. The system stores information about products, flavors, categories, suppliers, customers, purchases, sales, and inventory movements.

The database ensures data integrity through normalization and relational constraints while providing useful business reports using SQL queries.

---

# Technologies Used

- PostgreSQL 17
- SQL
- pgAdmin 4
- Git
- GitHub

---

# Database Engine

PostgreSQL

---

# Database Normalization

The database was normalized up to the **Third Normal Form (3NF)** to eliminate redundancy and improve data consistency.

## First Normal Form (1NF)

- Every table has a primary key.
- Each column contains atomic values.
- No repeating groups exist.

## Second Normal Form (2NF)

- All non-key attributes depend entirely on the primary key.
- Partial dependencies were removed.

## Third Normal Form (3NF)

- Transitive dependencies were eliminated.
- Categories, flavors, suppliers, cities, and units of measure were separated into independent tables.

---

# Database Structure

The database contains the following tables:

- Categories
- Flavors
- Units of Measure
- Products
- Cities
- Suppliers
- Customers
- Purchases
- Purchase Details
- Sales
- Sales Details
- Inventory Movements

---

# Entity Relationship Model (ERM)

The Entity Relationship Model establishes the relationships between all business entities.

Relationships include:

- One category has many flavors.
- One flavor has many products.
- One unit of measure has many products.
- One city has many suppliers.
- One supplier has many purchases.
- One purchase has many purchase details.
- One customer has many sales.
- One sale has many sale details.
- One product appears in many purchase details.
- One product appears in many sale details.
- One product has many inventory movements.

---

# Relational Model

## Categories

- id_category (PK)
- category_name

## Flavors

- id_flavor (PK)
- flavor_name
- id_category (FK)

## Units_of_Measure

- id_unit (PK)
- unit_name
- abbreviation

## Products

- id_product (PK)
- product_name
- description
- price
- stock
- id_flavor (FK)
- id_unit (FK)

## Cities

- id_city (PK)
- city_name
- department
- country

## Suppliers

- id_supplier (PK)
- supplier_name
- tax_id
- phone
- email
- id_city (FK)

## Customers

- id_customer (PK)
- customer_name
- phone
- email

## Purchases

- id_purchase (PK)
- purchase_date
- id_supplier (FK)

## Purchase_Details

- id_purchase_detail (PK)
- id_purchase (FK)
- id_product (FK)
- quantity
- purchase_price
- subtotal

## Sales

- id_sale (PK)
- sale_date
- id_customer (FK)

## Sales_Details

- id_sale_detail (PK)
- id_sale (FK)
- id_product (FK)
- quantity
- sale_price
- subtotal

## Inventory_Movements

- id_movement (PK)
- movement_date
- movement_type
- quantity
- id_product (FK)

---

# Installation Instructions

1. Install PostgreSQL.
2. Install pgAdmin 4.
3. Create a new database named **ice_cream_shop**.
4. Execute the SQL script.
5. Load the sample data.
6. Execute the SQL queries.

---

# Database Creation

The database was created using SQL Data Definition Language (DDL).

The project includes:

- CREATE DATABASE
- CREATE TABLE
- PRIMARY KEY
- FOREIGN KEY
- UNIQUE
- NOT NULL
- CHECK Constraints

---

# Data Loading Process

The database was populated using SQL INSERT statements.

The loading order was:

1. Categories
2. Flavors
3. Units of Measure
4. Products
5. Cities
6. Suppliers
7. Customers
8. Purchases
9. Purchase Details
10. Sales
11. Sales Details
12. Inventory Movements

This order guarantees referential integrity.

---

# SQL Queries

The project includes SQL queries that allow users to:

- View available inventory.
- Display the best-selling products.
- Calculate total sales by customer.
- Calculate total purchases by supplier.
- Display products grouped by flavor.
- Calculate average product prices.
- Find the most expensive product.
- Find the least expensive product.
- Display products with the lowest stock.
- Count products by category.
- Display daily sales.
- Calculate total sales revenue.
- Show complete sales details.
- Create business reports using JOIN, GROUP BY, ORDER BY, SUM, COUNT, AVG, MAX and MIN.

---

# Database Operations

The project also demonstrates the use of:

- INSERT
- UPDATE
- DELETE
- ALTER TABLE
- CREATE VIEW
- CREATE INDEX
- BEGIN
- COMMIT
- ROLLBACK

---

# Business Rules

- Every product belongs to one flavor.
- Every flavor belongs to one category.
- Every purchase must have one supplier.
- Every sale must have one customer.
- Inventory cannot be negative.
- Product prices must be greater than zero.
- Quantities must always be positive.

---

# Developer Information

**Full Name:** Kerlys Bello D.

**Course:** Software Development

**Database Management System:** PostgreSQL

**Programming Language:** SQL

---

# Project Author

Developed by **Kerlys Bello D.**
