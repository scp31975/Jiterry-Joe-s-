Group 7 Project Coffee Shop-

## Team Name

21479 Group 7

## Team Members

1. Sydney Pratt
2. Ally McVay https://github.com/allymcvay/JitteryJoes 
3. Casey Whichard https://github.com/caseywhichard/Team-7-MIST-4610-Group-Project-1
4. Mino Guzman https://github.com/Mino-Guzman/JitteryJoes

## Problem Description

The problem we have been tasked to solve is to design a data model and build a database that represents the relationships in operations of a global, multi‑location coffee chain. For this company, the Store serves as the central entity, since it is the physical center that connects customers to the products the coffee shop offers. The database also models the menu items and merchandise offered, suppliers of inventory, customer loyalty programs, and orders customers make. Using this data model, we generated realistic sample data that aligns with these entities and their relationships. By doing this, we are creating a database that allows us to perform relevant SQL queries that provide meaningful business insights that managers would be interested in, including company sales revenue, customer trends, and inventory levels.

## Explanation of Data Model

As mentioned above, our model is based on the structure of a global coffee chain. The Store is the central entity that represents each physical coffee shop location. Each store hires many employees, so we established a one‑to‑many relationship between the Store and Employees entities. Also, several pieces of inventory and equipment are assigned to one store, so there is a one‑to‑many relationship with the Store and Inventory and with the Store and Equipment entities as well. Finally, one store can take many orders from customers, so we created a one-to-many relationship between the Store and Order entities. 

What drives this business is sales, so customers interact with the business through order purchases. These purchases can consist of orders of food, drinks, and merchandise. We concluded that one customer can place many orders, so we created a one‑to‑many relationship between the Customers and Order entities. Orders can consist of merchandise as well, so using the same idea that one customer can purchase several pieces of merchandise, we placed a one-to-many relationship between the Customers and Merchandise entities. Finally, customers typically participate in the loyalty program to earn points with the hopes of getting deals on future purchases. Each customer can only have one loyalty account attached to their name, so this is modeled as a one‑to‑one relationship between the Customers and Loyalty entities.

Customers can make several payments on order purchases, since they can return to the store whenever they would like.So, we established a one-to-many relationship between the Customers and Payment entities. We also assume that each order only consists of one payment, so we created a one-to-one relationship between the Order and Payment entities. 

The company requires supplies on hand that go into inventory. In order to generate supplies, the company requires a supplier or suppliers to supply these items. Each supplier can ship several supplier items, which led us to establish a one-to-many relationship between the Suppliers and SupplierItem entities.

Overall, the data model, as shown below, successfully captures the relationships between the activities that take place in a global coffee chain. It provides a detailed understanding on the customer orders, inventory and equipment levels, the payment process, and hiring distributions. 

<img width="1017" height="1052" alt="image" src="https://github.com/user-attachments/assets/85790d04-a71f-4fb4-af8b-1e021697912e" />

## Data Dictionary

### Customers

<img width="946" height="921" alt="image" src="https://github.com/user-attachments/assets/a76200ca-374e-4043-9722-d576f2c1b409" />

### Employees

<img width="948" height="947" alt="image" src="https://github.com/user-attachments/assets/8bc6000a-d6b5-401a-a3ed-da19289d1d8d" />

### Equipment

<img width="924" height="841" alt="image" src="https://github.com/user-attachments/assets/1ca03214-aa69-4779-ba58-5d6681a45c46" />

### Inventory

<img width="929" height="940" alt="image" src="https://github.com/user-attachments/assets/3049ac3d-8f3f-40c9-a224-d4b4b38469d3" />

### Loyalty

<img width="980" height="891" alt="image" src="https://github.com/user-attachments/assets/67a610c6-30fe-4ce0-835e-1250ec89e80c" />

### Menu Item


### Merchandise

### Orders

### Order Item

### Payment

### Store

### Supplier Item

### Suppliers

## Queries

## Database Information

## Assumptions
