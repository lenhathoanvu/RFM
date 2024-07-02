# RFM Analysis

## Business case
You are invited to take on the role of Data Analyst for Meki Group - a coffee business chain headquartered in the USA with numerous branches worldwide. The company will provide you with raw datasets in .csv format regarding sales history and other information such as store details, customer information, employee data, and products the company is selling. Your task is to utilize your analytical skills and mindset to help Meki Group answer questions related to the company's business activities and make reasonable recommendations to enable Meki Group to make timely and accurate decisions.

## Datasets
### Dim_ustomer Dataset 
This dataset contains information about customers. Key columns include:
- ```customer_id```: Unique identifier for each customer.
- ```home_store```: Store ID where the customer primarily shops.
- ```gender```: Gender of the customer.
- ```customer_first_name```: First name of the customer.
- ```birthdate```: Birthdate of the customer.
- ```customer_email```: Email address of the customer.
- ```customer_since```: Date when the customer first registered or made a purchase.
- ```loyalty_card_number```: Loyalty card number associated with the customer.

### Dim_employee dataset 
This dataset contains information about employees. Key columns include:
- ```staff_id```: Unique identifier for each employee.
- ```first_name``` and ```last_name```: Employee's first and last names.
- ```position```: Job title of the employee.
- ```start_date``` and ```end_date```: Employment start and end dates.

### Dim_product dataset: 
This dataset provides details about products. Key columns include:
- ```product_id```: Unique identifier for each product.
- ```product_group```, ```product_category```, ```product_type```: Classification of the product.
- ```product```: Name of the product.
- ```product_description```: Description of the product.
- ```current_cost```, ```current_wholesale_price```, ```current_retail_price```: Cost and pricing details.
- ```unit_of_measure```: Unit measurement of the product.
- ```tax_exempt_yn```, ```promo_yn```, ```new_product_yn```: Flags indicating tax exemption, promotion status, and whether the product is new.

### Dim_store dataset
This dataset includes information about stores. Key columns include:
- ```store_id```: Unique identifier for each store.
- ```store_type```: Type of store (e.g., warehouse, retail).
- ```store_square_feet```: Size of the store in square feet.
- ```store_address```, ```store_city```, ```store_state_province```, ```store_postal_code```: Location details of the store.
- ```store_longitude```, ```store_latitude```: Geographical coordinates of the store.
- ```manager```: ID of the store manager.
- ```Neighorhood```: Neighborhood where the store is located.

### Historical_sales2020 dataset, Historical_sales2021 dataset, Historical_sales2022 dataset 
This dataset records sales transactions from 2021 to 2022. Key columns include:
- ```transaction_id```: Unique identifier for each transaction.
- ```transaction_date``` and ```transaction_time```: Date and time of the transaction.
- ```store_id```: Identifier of the store where the transaction took place.
- ```staff_id```: Identifier of the staff member who handled the transaction.
- ```customer_id```: Identifier of the customer who made the purchase.
- ```product_id```: Identifier of the product sold.
- ```quantity_sold```: Number of units sold.
- ```unit_price```: Price per unit of the product.
- ```promo_item_yn```: Flag indicating if the item was on promotion.

# Tableau - Dashboard 
[Link Dashboard](https://public.tableau.com/app/profile/l.nh.t.ho.n.v./viz/Meki-Group/Product?publish=yes)
## Data modeling:
- I have combined 3 sales tables into one large table ```Historical_sales``` to perform Data 
  ![image](https://github.com/lenhathoanvu/RFM/assets/173127058/7eb207a2-2a51-4f39-9929-86e15f96d766)

## Sales Overview for 6 months 
![image](https://github.com/lenhathoanvu/RFM/assets/173127058/a65b02a3-252c-4868-8db6-9369d1a6493c)
## Customer
![image](https://github.com/lenhathoanvu/RFM/assets/173127058/8bf7732b-81e4-4af7-9ebc-e47add332991)
## Employee 
![image](https://github.com/lenhathoanvu/RFM/assets/173127058/3986ffa0-41c8-4473-9c7e-aba7efd45c81)
## Product 
![image](https://github.com/lenhathoanvu/RFM/assets/173127058/fe083d5a-7919-43a9-a89b-77f894adf019)

# Python - RFM analysis: Customer Segmentation
[Link Code](https://github.com/lenhathoanvu/RFM/blob/master/RFM_Analysis_Meki_Group.ipynb)
## Method applied
- Data Cleaning
- Data Preprocessing
- Data Mining
- Data Clustering (K-means)
In this case, I will use RFM Analysis to segment customers. RFM (Recency, Frequency, Monetary) analysis is a marketing technique used to identify and categorize customers based on their purchasing behavior.

![image](https://github.com/lenhathoanvu/RFM/assets/173127058/a2d24983-47d4-4a70-a998-0280a443935a)

The three key components of RFM analysis are:
- ```Recency```: How recently a customer has made a purchase. Customers who recently purchased are more likely to buy again compared to those who haven't purchased in a while.
- ```Frequency```: How often a customer makes a purchase within a specific time frame. Customers who purchase more frequently are generally more loyal and engaged.
- ```Monetary```: The total amount of money a customer has spent. High-spending customers are often considered more valuable.
By scoring customers on each of these dimensions, businesses can segment their customer base, target marketing efforts more effectively, and ultimately increase customer retention and sales.
