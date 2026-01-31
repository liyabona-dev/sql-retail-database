SQL Retail Database – Project Requirements

1. Project Overview

This project simulates a retail order management database system designed
using SQL Server. The objective is to demonstrate the ability to translate
business requirements into a relational database design, enforce data
integrity, and generate meaningful business insights using SQL.

The system manages customers, products, orders, employees, and payments
within a structured and normalized database.

2. Functional Requirements

2.1 Customers
- The system shall store customer registration details.
- Each customer shall be uniquely identified.
- Each customer must have a unique email address.
- A customer may place multiple orders.

2.2 Products
- The system shall store product information including category and price.
- Each product shall have an available stock quantity.
- Product stock levels must not be negative.
- Products may exist even if they have never been sold.

2.3 Employees
- The system shall store employee details.
- Each order must be handled by one employee.
- An employee may handle multiple orders.

2.4 Orders
- The system shall allow customers to place orders.
- Each order shall be linked to one customer and one employee.
- Orders shall have a status: PENDING, COMPLETED, or CANCELLED.
- An order may contain multiple products.
- Orders may exist without payments.

2.5 Order Items
- Each order shall consist of one or more order items.
- Each order item shall reference a single product.
- Quantity and unit price must be recorded at the time of the order.
- An order item must belong to a valid order and product.

2.6 Payments
- The system shall record payment attempts for orders.
- An order may have multiple payment attempts.
- Payments may be successful or failed.
- Partial payments are allowed.
- Orders may exist with no payments.

3. Business Rules

- A customer cannot be deleted if they have existing orders.
- An order cannot be completed unless its total value has been fully paid.
- Only pending orders may be cancelled.
- Product inventory must reflect quantities sold.
- Foreign key relationships must be enforced to maintain data integrity.

4. Non-Functional Requirements

- The database shall enforce referential integrity using foreign keys.
- Constraints shall be used to validate data accuracy.
- Views shall be used to encapsulate business logic.
- Analytical queries shall be optimized for readability and performance.
- The system shall support reporting and analysis use cases.

5. Reporting & Analysis Requirements

- The database must support analytical queries that provide:
- Customer lifetime value analysis
- Product sales performance
- Employee sales contribution
- Identification of pending and problematic orders
- Financial summaries of orders and payments

6. Scope

In Scope:
- Relational database design
- SQL scripts for schema creation
- Sample data population
- Analytical queries
- Views for reporting
- Stored procedures and triggers (planned)

Out of Scope:
- User interface
- Authentication and authorization
- External system integrations
- Application-level logic

7. Assumptions

- The system is designed for learning and demonstration purposes.
- All monetary values are stored in a single currency.
- Time zones and tax calculations are not considered.