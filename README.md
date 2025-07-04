# <p align = 'center'> RFM Analysis

## Business case
You are invited to take on the role of Data Analyst for Meki Group - a leading FMCG company headquartered in the USA, with a wide portfolio of fast-moving consumer products distributed across multiple regions worldwide. The company will provide you with raw datasets in .csv format regarding sales history and other information such as store details, customer information, employee data, and products the company is selling. Your task is to utilize your analytical skills and mindset to help Meki Group answer questions related to the company's business activities and make reasonable recommendations to enable Meki Group to make timely and accurate decisions.

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

# Dashboard 
[Link Dashboard](https://public.tableau.com/app/profile/l.nh.t.ho.n.v./viz/Meki-Group/Product?publish=yes)
## Data modeling:
**Question:** Identify and describe the relationships between the tables in the Dataset sent to you
- I have combined 3 ```sales``` tables from 2020 to 2022 into one large table ```Historical_sales``` to perform Data 
  ![image](https://github.com/lenhathoanvu/RFM/assets/173127058/7eb207a2-2a51-4f39-9929-86e15f96d766)

## Sales Overview for 6 months 
**Question:** Mr. Brewer Mark, the CFO of Meki Group, is about to have a meeting with the Board of Directors to discuss some changes for the corporation. He needs you to provide an overview of Meki Group's business performance in the last 6 months. With your analytical skills, help Brewer Mark by providing key metrics such as revenue, profit, profit margin, and the percentage contribution of each store's revenue and profit to the total revenue.

![image](https://github.com/user-attachments/assets/826f36a2-405e-478c-bc9d-aa7e3906ea74)
**Insights:**
- Top Performer: Beverages are the top revenue and profit generators, contributing $785.01K in revenue and $588.43K in profit. Focus marketing efforts here.
- Store Performance: All three stores contribute almost equally to total revenue and profit, indicating consistent performance across locations.
- Trends: There's a noticeable dip in revenue and profit from November 2021 to January 2022, followed by a sharp increase in March 2022. Understanding these fluctuations can help in planning.
- High Profit Margin: The store maintains a strong profit margin of 74.05%, with total revenue of $1.02M and total costs of $264.06K in the last six months.

**Recommendations:**
- Emphasize Beverage Sales: Continue to promote and expand the beverage menu.
- Boost Underperformers: Increase marketing for food, whole bean/teas, merchandise, and add-ons.
- Analyze Fluctuations: Investigate the causes of monthly revenue and profit changes to stabilize future performance.
- Consistent Strategies: Apply successful strategies uniformly across all store locations.

## Customer
**Question:** Mr. LeBean Jean, the CEO of Meki Group, wants to gain a better understanding of the company's customer base (e.g., average age, gender, etc.). As a data analyst, help Mr. Jean with this task.

![image](https://github.com/user-attachments/assets/b7c7e985-9feb-4b10-a2e8-bc64dd7484c6)
**Insights:**
- Customer demographics: Largest age group is 23-34 (30.22%), and females make up the majority (43.38%) of customers.
- Customer loyalty: 44% of customers have been with the store since 2017.
- Peak hours: Highest customer traffic is between 8-10 AM.
- Store popularity: 100 Church Street is the busiest location with 946 customers.
- Average revenue per customer is $1,149.

**Recommendations:**
- Target marketing towards the 23-34 age group and female customers to capitalize on the largest customer segments.
- Implement a loyalty program to retain long-term customers and attract new ones.
- Optimize staffing and inventory during peak hours (8-10 AM) to manage the rush efficiently.
- Analyze the success factors of 100 Church Street and apply them to other locations, especially 687 9th Avenue.
- Consider extending operating hours earlier in the morning to capture potential customers before the 6 AM rush.
- Develop strategies to increase customer visits during slower hours (1-5 AM, 19-20 PM).
- Investigate reasons for the lower customer count at 687 9th Avenue and implement improvements.
- Create targeted promotions or products for different age groups to boost sales across all demographics.

## Employee 
**Question:** Help Meki Group calculate the total revenue and the average revenue per employee for Q1 of 2021. Then, compare these figures with Q1 of 2022. Assuming each employee receives a 5% commission on each order sold, how much commission has each employee received? Additionally?

![image](https://github.com/user-attachments/assets/38a0c807-fd58-4712-9a46-bb914898c946)
**Insights:**
- Overall revenue increased from Q1 2021 to Q1 2022 (409K to 425.74K).
- Britanni Jorden consistently leads in revenue and commission both years.
- The top 5 employees maintain their positions year-over-year.
- Average revenue per employee increased slightly (16.35K to 17.03K).
- Most employees show small growth in revenue from 2021 to 2022.

**Recommendations:**
- Analyze Britanni Jorden's strategies to potentially apply across the team.
- Focus on improving performance of lower-ranking employees through targeted training.
- Investigate reasons behind the overall revenue increase and capitalize on successful factors.
- Consider incentives or recognition programs to motivate continued growth.
- Evaluate commission structures to ensure they're driving desired behaviors and results.
- Look into any employees with declining performance (e.g., Aline Melanie) to address potential issues.
- Develop strategies to increase the average revenue per employee further.

## Product 
![image](https://github.com/user-attachments/assets/3aa48412-73ef-4379-8539-6ec249861c52)
**Insights:**

- Coffee is the highest revenue category, followed by tea and bakery items.
- Barista Espresso is the top revenue-generating product type.
- There's a significant gap between revenue and profit for most products, indicating high costs.
- Sustainably Grown Organic products (large and regular) are among the highest revenue items.
- Specialty drinks (e.g., Dark Chocolate, Latte, Cappuccino) perform well in revenue.

**Recommendations:**
- Focus marketing efforts on high-profit margin items, especially in the coffee category.
- Expand the sustainably grown and organic product lines due to their popularity.
- Analyze costs for products with large revenue-profit gaps to improve profitability.
- Consider promoting tea and bakery items more to boost their sales.
- Evaluate low-performing products (e.g., Packaged Chocolate, Flavours) for potential improvement or removal.
- Leverage the popularity of Barista Espresso to introduce complementary products or upsells.
- Investigate the success factors of top-performing products to apply to other offerings.

# Python - RFM analysis: Customer Segmentation
**Question:** One of Meki Group's key strategies in the near future is to improve and enhance the customer shopping experience, increase the number of new customers, and boost the retention rate of existing customers. Therefore, the company wants you to use your analytical skills to calculate and categorize new and loyal customers based on the purchase history in the provided dataset.

**In this case**, I will use RFM Analysis to segment customers. RFM (Recency, Frequency, Monetary) analysis is a marketing technique used to identify and categorize customers based on their purchasing behavior.
[Link Code](https://github.com/lenhathoanvu/RFM/blob/master/RFM_Analysis_Meki_Group.ipynb)
## Method applied
- Data Cleaning
- Data Preprocessing
- Data Mining
- Data Clustering (K-means)
- RFM method

![image](https://github.com/lenhathoanvu/RFM/assets/173127058/a2d24983-47d4-4a70-a998-0280a443935a)

The three key components of RFM analysis are:
- **Recency**: How recently a customer has made a purchase. Customers who recently purchased are more likely to buy again compared to those who haven't purchased in a while.
- **Frequency**: How often a customer makes a purchase within a specific time frame. Customers who purchase more frequently are generally more loyal and engaged.
- **Monetary**: The total amount of money a customer has spent. High-spending customers are often considered more valuable.

By scoring customers on each of these dimensions, businesses can segment their customer base, target marketing efforts more effectively, and ultimately increase customer retention and sales.

I wrote a Python script based on store transactions from 3 tables 2020-2022. The code will divide customers into the following groups:
- ```Best Customers```
- ```Loyal Customers```
- ```Big Spenders```
- ```Almost Lost```
- ```Lost Customers```
- ```Lost Cheap Customers```
![image](https://github.com/lenhathoanvu/RFM/assets/173127058/558ae291-bcd9-4bdf-9b50-bc34d01c3e7d)

### Some strategic development directions for the store

**Enhance Loyal Customer Care:**
- Reward Programs: Develop reward programs, discounts, or special offers exclusively for loyal customers to increase engagement.
- Personalized Services: Provide personalized services, such as sending birthday wishes or special gifts on significant occasions.
  
**Attract High-Spending Customers:**
- Exclusive Offers: Provide exclusive offers and VIP customer programs for high-spending groups.
- Premium Products/Services: Introduce additional premium products or services to meet the needs of this customer group.

**Recover Nearly Lost Customers:**
- Feedback Surveys: Send feedback surveys to understand why customers almost left and improve weak points.
- Promotional Campaigns: Implement promotional campaigns aimed at enticing them to return, such as discounts or gifts when they shop again.

**Reduce Customer Attrition:**
- Analyze Reasons: Analyze the reasons for customer attrition and take measures to address them, such as improving product or service quality.
- Promotional Programs: Create attractive promotional programs to retain customers.

**Optimize Best Customer Care:**
- Priority Services: Provide priority and special services for the best customer group to enhance satisfaction and loyalty.
- Loyalty Programs: Ensure this customer group always benefits from loyalty programs and feels valued.

**Marketing Strategy for Potential Customers:**
- Marketing Campaigns: Build marketing campaigns targeting potential customers based on the profile of current customers.
- Targeted Advertising: Use targeted advertising on online platforms to reach potential customer groups.

**Improve Overall Customer Experience:**
- Employee Training: Enhance employee training on customer service to ensure every customer has the best experience when visiting the store.
- Service Improvement: Continuously improve service and product quality based on customer feedback.
