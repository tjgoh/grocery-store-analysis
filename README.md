# Statistical analysis of grocery store data

This file grocery-store-data.csv contains a sample of sales and promotional information of 12 products from a set of grocery stores over a subset of a period of 156 weeks from Jan 2009 through to December 2011. All 12 products belong to the frozen pizza category. The file contains the following variables:

| Variable name | Description                                                                                                  |
| ------------- | ------------------------------------------------------------------------------------------------------------ |
| BASE_PRICE    | Regular price of item                                                                                        |
| PRICE         | Actual amount charged for the product at shelf                                                               |
| WEEK_END_DATE | Week endind date                                                                                             |
| STORE_NUM     | Store number                                                                                                 |
| UPC           | (Universal Product Code) Product specific identifier                                                         |
| MANUFACTURER  | Manufacturer                                                                                                 |
| DISPLAY       | Product was a part of in-store promotional display                                                           |
| FEATURE       | Product was in in-store leaflet                                                                              |
| TPR_ONLY      | Temporary price reduction only (i.e. product was reduced in price but not on display or in an advertisement) |
| UNITS         | Units sold                                                                                                   |

The response variable is UNITS i.e., how many units of that product were sold in a particular week at a particular store. A linear model and an advanced regression model were built to preduct UNITS given the available covariates, and to compare whether one is signigicantly better at predicting the response than the other.
The project is loosely organised as follows:

- Summary statistics
- A linear model is fit that enables UNITS to be predicted from other covariates
- An advanced regression model is fit to predict UNITS from other covariates
- 10-fold cross validation is performed for each model and a t-test is carried out to assess which model is better
- The final model is used to predict the average effect of decreasing PRICE by 10% on a partiular product

The code can be found [here](https://github.com/tjgoh/grocery-store-analysis/blob/main/grocery-store-analysis.Rmd) and the corresponding report can be found [here](https://github.com/tjgoh/grocery-store-analysis/blob/main/grocery-store-analysis.md).
