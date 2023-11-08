# Udacity_Blog_and_Git_Post
 For my Blog and Github Posts

1. Data
Sourced:		Kaggle on 2023/11/06 (ref: https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset)
Description: 	
Context - 
				Welcome to the shopping world of Istanbul! Our dataset contains shopping information from 10 
				different shopping malls between 2021 and 2023. We have gathered data from various age groups and genders to provide a 
				comprehensive view of shopping habits in Istanbul. The dataset includes essential information such as invoice numbers, 
				customer IDs, age, gender, payment methods, product categories, quantity, price, order dates, and shopping mall locations. 
				We hope that this dataset will serve as a valuable resource for researchers, data analysts, and machine learning enthusiasts 
				who want to gain insights into shopping trends and patterns in Istanbul. Explore the dataset and discover the fascinating world of Istanbul shopping!

Content - 
				invoice_no: Invoice number. Nominal. A combination of the letter 'I' and a 6-digit integer uniquely assigned to each operation.
				customer_id: Customer number. Nominal. A combination of the letter 'C' and a 6-digit integer uniquely assigned to each operation.
				gender: String variable of the customer's gender.
				age: Positive Integer variable of the customers age.
				category: String variable of the category of the purchased product.
				quantity: The quantities of each product (item) per transaction. Numeric.
				price: Unit price. Numeric. Product price per unit in Turkish Liras (TL).
				payment_method: String variable of the payment method (cash, credit card or debit card) used for the transaction.
				invoice_date: Invoice date. The day when a transaction was generated.
				shopping_mall: String variable of the name of the shopping mall where the transaction was made.

2. Business Objectives
Suppose a new entrepreneur wishes to open a shop in Istanbul but they do not know where to setup shop, what to sell nor understand the customer demographics and shopping tendancies. 
Below are some questions that the entrepreneur might ask in order to make well informed decisions.
Based on this historical data;
2.1 What might be the best location to setup the shop?
2.2 What goods might be worthwhile selling?
2.3 3. Can demand be expected to vary between males and females?

3. Data Wrangling and Cleaning
In helping answer the entrepreneur's questions above, the data is wrangled and cleaned with respect to each question asked. That is to say, 
3.1 To determine the best mall for the entrepreneur, consider analyzing the 3 columns including the shopping_mall, price and quantity.
	If the mall name is missing or price or quantity <= 0, drop the row as it does not help answer the question.
3.2 Here, the columns of interest would be category and quantity. So if category is missing or quantity <= 0, remove row from analysis.
3.3 This question demands investigating gender and quantity of products purchaed. As such, rows of missing gender or quantity <= 0 are ignored.
3.4 The primary variable to consider here would be the age of the shoppers. So any outlier age(s) ought to be rmeoved from the data.

4. Data Analysis
4.1 For all analyses, the following Python libraries were used:numpy, pandas, matplotlib.pyplot and seaborn

5. Results, Interpretation and Conclusion
Much of the analysis carried out is descriptive, however, the conclusions are light inferences based on these results so as to be able to answer the questions posed.
5.1. To answer the first question, it was necessary to understand if any of the Malls generally sold relatively lots of goods cheaply or on the other streme, 
	 sold few but expensive items. To help in this led to analysing the weighted average item cost price per mall. This was found to be roughly the same 
	 across malls at around 842 or, proportionally, about 10%. What this implied was that the the quantity of goods sold would be most indicitive of the 
	 mall that sell the most number of items. This happens to be The Mall of Istanbul which sold about 20.1% of all units with Kanyon close behind at 19.9%. 
	 
5.2 The product categories to invest in once the shop is located in the Mall of Istanbul is Clothing as it has the most items bought at roughly 35%. 
	In second and third places would be Cosmetics and Food&Beverage with 15.3% and 14.8% of the units sold respectively. Together these categories amount to about 65%
	of all units sold at this particular mall.
	
5.3 The average number of items consumed by males versus that consumed by females is roughly the same at approx 3 with a standard deviation of 1.4. It stands to reason 
	that males and females show the same demand for goods. 

6. Conclusion
In Conclusion, the entrepreneur will be well advised to open their shop in the Istanbul Mall where they can immediately start selling Clothing, Cosmetics and Food&Beverage as 
these product categories have shown to be a significant proportion of the market. Though gender might play a role in the buying tendancies of the cutomers, ultimately,
the demand is relatively symmetrical. As result, keep enough stock of each product category at all times.   
