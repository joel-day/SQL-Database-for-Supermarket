# SQL-Database-for-Supermarket
SQL &amp; Python

# Data
This data set is small enough to store on a local MySQL server, but complex enough to practice feature transformations, create complex views, and resemble real-world supermarkets. The data was originally web scraped by Karanth in 2020 but downloaded from kaggle. The executable, in its current state, is designed to be run on a per instance basis. The schema is static; in other words, the CSV files must adhere to the current structure to be properly ingested.

## Supermarket Database EER Diagram
![image](https://github.com/joel-day/SQL-Database-for-Supermarket/assets/105340191/e223bfd5-7649-4e37-8b6d-7e03e8eeab29)

The database schema diagram is a visual representation of the structure of the supermarket database and the relationships between its tables. It represents a supemarket’s order,
invoice, and sales data. There are four tables present: customer_order, salesteam, orders, and invoice. The customer_order table was derived from two source tables, orders and invoice, and
allows for the user to easily identify each unique order id attributed to a particular customer. The salesteam table contains information about the sales team responsible for handling the invoices and orders. The orders table stores information about the supermarket’s order leads. The invoice table stores information about the invoices issued by the supermarket.

The customer_order, salesteam, and invoice tables are related to the orders table as it provides data about orders placed at a supermarket. The customer_order and orders table have a
many-to-one relationship as multiple order leads can belong to the customer. The salesteam and orders table have a many-to-one relationship as multiple order leads can belong to the same sales
team. The salesteam and invoice tables have a many-to-many relationship as multiple invoices can be handled by a single or multiple sales teams. The orders and invoice tables have a
one-to-many relationship as one customer can have multiple invoice and order leads. The compound primary key for the orders table, built on the fields order_id and company_id, also
acts as the references for the other tables’ foreign keys on one of the two fields.
