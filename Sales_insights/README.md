
## Dashboard
<img src="https://github.com/Mukul-MV/Power-Bi-Projects/blob/main/Sales_insights/Revenue%201.png?raw=true" alt="revenue" width="500"/><img src="https://github.com/Mukul-MV/Power-Bi-Projects/blob/main/Sales_insights/Profit%20MArgin%202.png?raw=true" alt="Profit Margin" width="500"/>
 




# Sales -Analysis with Power BI dashBoard

## Introduction
This is an analysis of the sales data on Power Bi Software
with particular focus given to how promotions and 
 advertising translate into sales, in terms of 
 both units sold and sales INRs.


##  Purpose of this Project
To unlock sales insights that are not visible before for sales teams for
decision support & automate them to reduced manual time spent on data
gethering.

## Success Criteria
* dashBoard uncovering sales order insights with latest data available.
* Sales team able to take better decision & prove 10% cosr savings of total spend.
* SAles Analysts stop data gathering manually in order to save 20% of thier business time and reinvest it value added activity.

## End Result

An Automated Dashboard providing quick & latest sales insights in order
to support data driven decsion making.
## Roadmap

- **Data Exploration**
```
Taking a look at the categorical and continuous feature summaries and making inferences about the data.
```

- Data Cleaning 
```
Imputing missing values in the data, removing duplicates, and checking for outliers.

Like,

- INR and USD two currencies are present then convert into one currency 

- Sales value somewhere is negative and zero. So removed those outliers
```
- Feature Engineering
```
Modifying existing variables and creating new ones for analysis.

Like , 

- Creation of sales_INR column to make only one transaction currency.

- Total revenue, total profit margin, Percentage of profit margin, and revenue margin contribution.
```
- Model Building
```
Making predictive models on the data.

In this, there is one fact table i.e "sales transaction" and others are dimension tables i.e "sales market" , "sales product" , "sales date" and "sales customers" . 

So, it makes the Star Schema model.
```
- Hypothesis Generation 
```
Brainstorm possible factors that may influence the outcome of the problem to better understand it.
```

## Data Analysis Using SQL

1. Show all each table records :- below example of customer table
```bash
  SELECT * FROM customers;
```

2. Show total number of records :- below example of customer table
```bash
  SELECT count(*) FROM customers;
```
3. Show transactions for Chennai market
```bash
  SELECT * FROM TRANSACTIONS T INNER JOIN MARKETS M 
  ON T.MARKET_CODE = M.MARKETS_CODE
  WHERE M.MARKETS_NAME = "CHENNAI"

```
4. Show distrinct product codes that were sold in chennai
```bash
  SELECT distinct(t.product_code) FROM TRANSACTIONS T INNER JOIN MARKETS M 
  ON T.MARKET_CODE = M.MARKETS_CODE
  WHERE M.MARKETS_NAME = "CHENNAI"

```
5. Show different Currencies
```bash
SELECT * FROM TRANSACTIONS WHERE CURRENCY="USD"
```
6. Show total revenue in year 2020,
```bash
SELECT SUM(SALES_AMOUNT) FROM TRANSACTIONS
WHERE YEAR(ORDER_DATE) = 2020 

```


## Data Analysis Using Power BI

1. Formula to create sales_INR column
```bash
  = Table.AddColumn(#"Filtered Rows", "sales_INR", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*78 else [sales_amount], type any)
```

2. Profit Margin Contribution
```bash
  
```
3. Revenue Contribution
```bash
  

```
4. Total Profit Margin % 
```bash
  

```

## Project Deployment

Used Data set [SQL database](https://github.com/Mukul-MV/Power-Bi-Projects/blob/main/Sales_insights/db_dump.sql)

Power BI [Dashboard](https://app.powerbi.com/links/DknGjZxZ1o?ctid=e36b8a1b-051b-47f5-b580-382f4571c8fb&pbi_source=linkShare)

Power BI report Dashboard [PDF](https://drive.google.com/file/d/1Z3UA-9-1S5L8u62Fn4Fz6zidrXu0wlb0/view?usp=sharing)

## Demo

Insert gif or link to demo

![v](https://drive.google.com/file/d/1Hj3AYdOrLi-AbQoxofMu-oHTMV7W5Oda/view?usp=sharing)
