# Multifamily Regression analysis

The last decade has seen a proliferation of rent increases in the multifamily space.  We wanted to know on average, how many tenants are likely to move out with a rent increase.  To do this, we took data from four multifamily properties in four different Midwest cities, including Chicago, Columbus, Dayton and Toledo, OH.  
Each rental market has it’s own discrete drivers , dynamics and tenant base, which, taken together, provides a holistic view of the rental market in the Midwest.  The data was taken from a period of April 2013 to January 2019.

## Data Acquisition and Cleaning

We acquired the data from actual properties, using CSV files generated from a MS SQL-based database system.  Our main CSV file was a Tenant_History file that contained a wide .  We eliminated all but the Move In, Move Out and Rent Change events for all properties.  The biggest challenge was to get unit occupancy.  We had to use a calculated field for this, taking the move in less the move out columns.  The time between those dates is considered to be occupied date.

## Model Building

We used two regression models in our study- one linear regression model, and one logistic model.   The logistic model predicted unit vacancy based upon rent changes

For the linear regression, we created a “Rent Predictor”, which would look at historical data and provide a forecasted rent based on several key inputs, including number of bedrooms, bathrooms   We binned the unit sizes based on square footage to small medium and large.  We then one-hot encoded the data.

