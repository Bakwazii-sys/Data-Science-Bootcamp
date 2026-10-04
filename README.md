# Data-Science-Bootcamp
The project is a production-ready Relational database schema and Entity-Relationship Model designed for WitleShop (Pty) Ltd, that sells electronics, clothing, and home appliances directly to customers through a web and mobile platform (e-commerce).

About This Project
As online sales scale, e-commerce platforms require a database schema that guarantees data integrity, eliminates redundancy, and handles high-volume transactions smoothly.

This repository contains the complete relational database design (ERD) for WitleShop (Pty) Ltd. It provides a standardized data model covering everything from customer onboarding and multi-address management to inventory, payments, and courier dispatch.

Entity Relationship Diagram

Image
Entities were Identified to pinpoint all core business entities and necessary database tables needed for the retail system. The Primary Keys (PK) for unique record identification and Foreign Keys (FK) were also identified as well as their relationships & Cardinality as either One-to-One, One-to-Many, or Many-to-Many.

Brief breakdown of the above ERD:

Customer
• PK: customer_id
• Attributes: full_name, email, phone_number, date_registered
Customer_Address
• PK: address_id
• FK: customer_id
• Attributes: street_address, city, province
Orders
• PK: order_id
• FK: customer_id
• Attributes: order_date, order_status, total_amount
Order_Item
• PK: order_item_id
• FK: order_id, product_id
• Attributes: item_quantity, unit_price
Product
• PK: product_id
• FK: category_id, supplier_id
• Attributes: product_name, product_description, price, stock_quantity
Payment
• PK: payment_id
• FK: order_id
• Attributes: payment_date, payment_status, payment_method, amount_paid
Delivery
• PK: delivery_id
• FK: order_id, address_id
• Attributes: delivery_date, deilvery_status, tracking_number, courier_name
Supplier
• PK: supplier_id
• Attributes: supplier_name, supplier_email, phone_number
Category
• PK: category_id
• Attributes: category_name, category_description
