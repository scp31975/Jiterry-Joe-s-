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

<img width="934" height="614" alt="image" src="https://github.com/user-attachments/assets/0aac0ace-1187-4aae-82a9-74f659a6aa93" />

### Merchandise

<img width="919" height="885" alt="image" src="https://github.com/user-attachments/assets/b2581c59-af4f-49eb-a701-8fbfdddbd12c" />

### Order Item

<img width="945" height="926" alt="image" src="https://github.com/user-attachments/assets/04a21b99-af5d-4ce8-88a5-1997412394ab" />

### Orders

<img width="935" height="1057" alt="image" src="https://github.com/user-attachments/assets/e1dd9420-baef-41a3-a98d-628be7bbf7a5" />

### Payment

<img width="913" height="1053" alt="image" src="https://github.com/user-attachments/assets/3ce55239-d58c-4e34-8b22-af4c313f9530" />

### Store

<img width="935" height="533" alt="image" src="https://github.com/user-attachments/assets/96b9b817-aaab-4cb4-8b45-a532958b4808" />

### Supplier Item

<img width="910" height="744" alt="image" src="https://github.com/user-attachments/assets/caf05f5c-505e-4210-bef3-1652cdd2b72b" />

### Suppliers

<img width="915" height="657" alt="image" src="https://github.com/user-attachments/assets/b457e027-01e2-4e84-9b7b-3938b80b8853" />

## Queries

Query 1: List all cafe managers that are seasonal
<img width="1301" height="857" alt="image" src="https://github.com/user-attachments/assets/2e98f38e-422f-4ec4-96c2-fa4104894ea2" />
This query retrieves all employees, who are managers, that work seasonal. Seasonal managers typically work only during peak periods, such as the academic year or high‑traffic months. Knowing exactly who these managers are helps the organization anticipate staffing gaps when the season ends. 

Query 2: Show all items on the menu that have never been ordered
<img width="1284" height="897" alt="image" src="https://github.com/user-attachments/assets/1acaf4de-01df-49d4-a823-0fe96236984e" />
This query helps managers identify which menu items have never been purchased. Items with zero orders may signal low visibility, poor appeal, or unnecessary complexity on the menu. By isolating these products, managers can decide whether to market them, adjust pricing, or remove them to reduce wasting resources.

Query 3: Show all orders and status
<img width="1277" height="998" alt="image" src="https://github.com/user-attachments/assets/89f2752c-ec7c-48c0-9301-f4daf1ff6b9d" />
This query pulls information from the SupplierItem and Suppliers tables to show what items have been shipped, when they were shipped, and the status of the supplier. It is useful in providing visibility into the supply chain and helping track incoming inventory.

Query 4: Show revenue by payment type
<img width="1214" height="849" alt="image" src="https://github.com/user-attachments/assets/732279b6-bc19-48b3-9f07-191d070d040f" />
This query shows how much revenue comes from each card type, helping managers understand which cards customers use most. This makes it easier to plan for reliable payment processing, manage card‑related fees, and ensure the systems support the most common payment methods efficiently.

Query 5: Find the average order value by store
<img width="1202" height="875" alt="image" src="https://github.com/user-attachments/assets/538cb491-c9ab-4db9-8c77-ddc9b9719cd3" />
We took the value of the average order from each store. By doing so we were able to retrieve each store's location alongside three performance metrics: the number of orders it received, the average value of each order, as well as the total revenue generated. The results are sorted in a descending order based on the average order value.

Query 6: Find the most popular menu items by total quantity sold
<img width="1182" height="842" alt="image" src="https://github.com/user-attachments/assets/5103cfc5-89ab-4b5d-b858-7ac127f372ad" />
We ranked the popularity of each item based on the item’s total quantity sold.
The query ranked each menu item by the number of units sold across all orders, while also calculating the total revenue generated from each item. The information provided became a useful way to identify bestsellers and top revenue-driving items.

Query 7: Show stores with above average revenue
<img width="1183" height="877" alt="image" src="https://github.com/user-attachments/assets/5c16af05-0868-4a54-bbe2-f58f82495478" />
Query 7 filters through all the stores and selects the stores whose total revenue exceeds the average revenue across all stores. By using a subquery first we were able to calculate each store's total, then averaged those totals as the benchmark.

Query 8: Show stores with low inventory that need to reorder
<img width="1190" height="874" alt="image" src="https://github.com/user-attachments/assets/009c0572-ce21-49b9-a395-3f7e42633e7a" />
The query scans all of the  inventory records and provides any item at a store whose current quantity has fallen below the reorder level. While also calculating exactly the number of units that need to be ordered in order to get back to the designated threshold, sorted by most urgent need first.

Query 9: Show the customer who spend the most
<img width="1236" height="879" alt="image" src="https://github.com/user-attachments/assets/6b9120f2-fe1a-48b1-965b-d68f5f956918" />
Identifies the individual customer who has the highest total, meaning they spent the most in total across all their orders. The subquery finds the maximum customer total and then matches that specific value back to the customer's name and ID.

Query 10: Find which menu items generate above average revenue
<img width="1224" height="928" alt="image" src="https://github.com/user-attachments/assets/861b4e26-b1ce-4e82-816b-e317cdbc80cd" />
Like Query 7, Query 10 provides us with the menu items that bring in an above average total revenue. However, in this case it is focused on menu items rather than stores. Calculating each item's total revenue while only returning those that exceed the average revenue per item, helping identify the strongest performers on the menu.

<img width="1273" height="800" alt="image" src="https://github.com/user-attachments/assets/27abc93c-0b79-4619-b4fc-59f3c16256db" />

## Database Information

MySQL server: al_Group_21479_G7

## Assumptions

LoyaltyID is stored redundantly in order to keep track of loyalty at the time of a purchase, since customer loyalty status can change over time.
