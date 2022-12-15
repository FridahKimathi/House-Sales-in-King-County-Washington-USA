
<img src="images\King_county_houses.jpeg" alt="A picture of houses in King County, USA" width="400" height="250">

# House Sales in King County, USA

**Author**: [Fridah Kimathi](mailto:fridahnkirotekimathi@gmail.com)

## Overview
The project analyzes about 21597 houses sold in King County, Washington-USA in the years 2014 and 2015.
 The relevant features in the dataset used for analysis and linear regression in this project are; house id, date, house price, number of bedrooms and bathrooms, size of living space and property, number of floors the house has, the condition and grade of the house according to the King County System and the year the house was built. 

## Business Problem

The project aims to aid a Real Estate Agency in King county, Washington-USA predict the house prices for single-family homes that their potential clients are looking buy and/or sell. The business problem the project aims to tackle is to highlight the main influential factors affecting a home's value in King county, Washington-USA. 

## Data

The King County Housing Data Set contains information about the size, location, condition, and other features of houses in Washington's King County. More details about the columns can be found in <a href="https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r"> King County Residential Glossary of Terms </a> 

## Methods
After exploring, splitting and preprocessing the data, multiple linear regression models were built with price as the dependent variable.

## Results

The price of the house is relatively highly correlated to two columns, that is footage of the home(sqft_living) and grade
<img src="images\heatmap_corr.jpg"> 

Features such as number of bedrooms and bathrooms, size of living space and property, number of floors the house has, whether the house has a waterfall or not and the grade of the house  were included in the final multiple linear regression model. 
<img src="images\scatterplot.png"> 

The model satisfied all linear regression assumptions that is linearity, normality, multicollinearity and homoscedasticity.
           Linearity Assumption
<img src="images\Linearity.png">  
           Normality Assumption
<img src="images\Normality.png">
           Homoscedasticity Assumption
<img src="images\Homoscedasticity.png">

 The p-values for each predictor variable were below 0.05 and therefore the null hypothesis that states that there is no relationship between the chosen explanatory variables and the response variable can be rejected. The r-squared value of the model was 0.63.

## Conclusions

This analysis leads to three recommendations for improving operations of the Austin Animal Center:

- **Homeowners interested in selling their homes should focus on improving the design and quality of construction of their homes** This may in turn improve the grade of the home.
- **Home buyers looking to buy a house should consider older homes with a high grade** Older home tend to be slightly cheaper. If a home is old and has a high grade, this might be one of the cheapest yet good quality homes the buyer will find. Home with a low number of bathrooms tend to be cheaper too.
- **If possible, homeowners should also expand the square footage of living space on the lot**  The higher the sqaure footage of the living space, the higher the house sale price.

## Limitations

The model does have some limitations such as; some of the variables needed to be log-transformed to satisfy regression assumptions hence any new data used with the model would have to undergo similar preprocessing. Additionally, given that outliers were removed, the model may also not accurately predict extreme values. Future analysis should explore the best predictors of the prices of homes outside of King County, as well as homes with extreme price values.

### Next Steps

Further analyses could yield additional insights to further improve operations at AAC:

- **Prediction of house price based on the crime rate of the neighborhood where the house is located**This model could use already available data, such as latitude and longitude coordinates, and police records.

- **Prediction of house price based on the the average income of residents of the county** This model could predict house prices based on the average income of residents of the area.

- **Prediction of house price based on the ethnicity and race of the residents in an area** This model could identify the effect of ethnic-racial discrimination on house prices

## For More Information

See the full analysis in the [Jupyter Notebook](./animal-shelter-needs-analysis.ipynb) or review this [presentation](./Animal_Shelter_Needs_Presentation.pdf).

For additional info, contact Fridah Kimathi at [fridahnkirotekimathi@gmail.com](mailto:fridahnkirotekimathi@gmail.com) or via my [LinkedIn profile](https://www.linkedin.com/in/fridah-kimathi-91608418b/).



## Repository Structure

```
├── data
├── images
├── README.md
├── Animal_Shelter_Needs_Presentation.pdf
└── animal_shelter_needs_analysis.ipynb
```