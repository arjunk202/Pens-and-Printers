Business Problem Definition
The business problem at hand is to determine the most effective sales strategy for Pens and Printers' new line of office stationery. The company has tested three different sales strategies, namely email, phone calls, and a combination of email and phone calls, to sell the new product line. The sales team needs to understand which approach worked the best and if there were any differences in revenue over time for each of the methods. Additionally, the team wants to identify if there are other differences between the customers in each group that could provide context for what went well. The goal is to use the findings to inform the decision of which sales strategy to continue using to sell the new product line.

Data validation
This step starts with performing data prepration tasks including removing duplicates, dealing with missing values, and transforming variables. The dataset contains 15,000 rows and 8 columns before cleaning and validataion. I have validated all the columns against the criteria in the dataset table:

Here's a breakdown of each column's validation and cleaning steps:

"Week": The "Week" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column. Unique values: 6
"Sales Method": The "Sales Method" column is validated by checking the unique values and the number of missing values. No cleaning is performed on this column. Unique values: ['Email + Call' 'Call' 'Email' 'em + call' 'email' ]
"Customer ID": The "Customer ID" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column. - Unique values: 15000
"Number of Products Sold": The "Number of Products Sold" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column.
"Revenue": The "Revenue" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column. Unique values: 6743
"Years as Customer": The "Years as Customer" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column. Unique values: 42
"Number of Site Visits": The "Number of Site Visits" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column. Unique values: 26
"State": The "State" column is validated by checking the number of unique values and the number of missing values. No cleaning is performed on this column. Unique values: 50
Data types of all columns are validated.
After validating each column, two cleaning steps are performed on the entire dataset:

Repalcing missing values with median of revenue column: Rows with missing values are repalced with median of revenue column using the fillna() method. We replaced 1074 missing values in revenue column.
Remove duplicates: Duplicate rows are removed from the dataset using the drop_duplicates() method. we didn't find duplicates in the dataset.
After two cleaning steps, we transform the sales_method column:

We use the replace function to replace all occurrences of 'em + call' with 'Email + Call' and 'email' with 'Email' in the sales_method column. So, we have only three columns representing the sales method 'Email + Call', 'Call', 'Email'

After the data validation, the dataset contains 15000 rows and 8 columns.
