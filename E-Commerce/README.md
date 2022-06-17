
## Screenshots ![](https://media.giphy.com/media/l46Cy1rHbQ92uuLXa/giphy.gif)

![Revenue](https://drive.google.com/file/d/1Xbfd_0mfiP4-Ag6U7qRVHi45XNWX1f-O/view?usp=sharing)

![Profit Margin](https://drive.google.com/file/d/1JcnRt8mPFB3gLp-_HKINID8Ksee1ridm/view?usp=sharing)


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

## Deployment

To deploy this project run

```bash
  npm run deploy
```


## Running Tests

To run tests, run the following command

```bash
  npm run test
```


## Usage/Examples

```sql
sql
```


![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)


## Installation

Install my-project with npm

```bash
  npm install my-project
  cd my-project
```
    
## Demo

Insert gif or link to demo

