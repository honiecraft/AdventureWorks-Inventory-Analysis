# AdventureWorks Inventory Analysis [Power BI]
This project aims to **build Dashboard using Power BI** to give a complete and understandable picture of the **warehouse data**, from there provide ideas, insights, and suggestions to stakeholders.

## About
**AdventureWorks** database supports standard online transaction processing scenarios for a *fictitious bicycle manufacturer* - **Adventure Works Cycles**. Scenarios include *Manufacturing, Sales, Purchasing, Product Management, Contact Management, and Human Resources*.

The warehouse department of a business is responsible for storing goods including finished products, semi-finished products, and raw materials for production.
Warehouses are located in many different locations for convenience and optimization of storage and distribution to customers.
- **Warehouse managers and warehouse staff** need to *closely monitor and control the amount of goods in the warehouse, ensuring that goods are stored at prescribed levels*.
From there, build appropriate strategies to better manage and operate storage activities.
- **Sales people and the Marketing team** also need to *monitor the amount of goods in the warehouse to build, control, and adjust sales and marketing campaigns accordingly*.

> **Objective**\
> Building Dashboard for stakeholders to have a complete and easy-to-understand picture of warehouse data, helping them make better decisions and operations.
In addition, providing ideas, insights, and suggestions to those stakeholders.

## Dataset  
- Project used dataset of AdventureWorks from BigQuery, to **connect BigQuery with PowerBI**, please follow [this](https://learn.microsoft.com/en-us/power-query/connectors/google-bigquery) instruction.
- Once connected successfully, select dataset `adventurework2019` and the tables needed to load into Power BI.
- Tables used:
  - **Product** [fact]
  - **Location** [dim]
  - **ProductInventory** [dim]
  - **ProductCategory** [dim]
  - **ProductSubcategory** [dim]
- Click [here](https://dataedo.com/download/AdventureWorks.pdf) to view **Table Schema**.

## Data Model
![image](https://github.com/user-attachments/assets/10162b77-ae3b-425a-8014-ea0d65eda0f7)

## Dashboard
### 1. Overview
![image](https://github.com/user-attachments/assets/a354c8dc-4326-4756-bc78-005e37b6b8f6)

### 2. Product Information
![image](https://github.com/user-attachments/assets/2a0a761b-2c77-473a-94dd-8ff233b7ee1d)


## Insight
- The **Total number of products in stock** of the company is 504 products, of which (363 products are at the Safe level, 61 products are Below the Safety level, 4 products need to be Reordered, 76 products are Out of Stock)
- The **total quantity of goods** is 336k with the **highest number of nonsalable items (category Other)** 76.84%, Components (14.05%), Bikes (4.62%), Accessories (2.72%), Clothing (1.77%)
- **Inventory value:** total inventory value is 20m, in which _Category Bike has the lowest quantity but the highest value_ compared to the remaining categories (14.6m), on the contrary, _category Other has the highest quantity but the value is relatively low_ (867k).
- **Make status:** Category **Accessories and Clothing** are completely **purchased** products, most of the nonsalable items are also purchased. The company only **produces category Bikes**, most of the Components and some Other categories
- **Location:**
  - Location **Subassembly, Miscellaneous storage, Tool Crib** are the 3 areas that **contain the most products** (mainly _nonsalable_ items, Components and a few Accessories);
  - Finished Goods Storage contains Bikes, Accessories, Clothing;
  - Bikes are also in the Final assembly location;
  - The remaining areas store Components and Other items;
- **Stock status:**
  - Most are **Safety** status;
  - **Below safety** falls mainly in Other category (25%) and Accessories (10%);
  - **Outstock** items are mostly in Component category (53.72%), few in Clothing (8.57%);
  - **Reorder** quantity is very low (1 Bike product, 2 Other products, 1 Components product).
- **Overstock**: There are some products with very **high inventory compared to the set safety level** (up to 80x), mainly from Clothing and Accessories items (purchased products).

## Recommend
- Check the **reasons for overstock items** (buying in reserve, slow-moving goods or safety level set too low);
- Monitor daily alert metrics to promptly add out stock products, reorder, and note products under safety.
