**IMMO-ELIZA-TEAM2**
## Team members:
Team leader: Urson

Repo manager: Moustafa

Developpers:
Majid, Minh, Dhrisya

## Mission's summary

The real estate company Immo Eliza wants to establish itself as the biggest Belgian real estate services provider. To achieve that goal, they need to more accurately and faster than their competitors estimate the value of properties, to pick out those properties that are most valuable to them and their clients.

Enter creating a machine learning model to predict the prices of properties across Belgium. Having no in-house data scientists, they are looking for talented people to do it for them. Since your last encounter with them went great, they continue to rely on you to do the job. Everything is in your hands now!

By the end of this week, Immo Eliza's management wants to see a preliminary analysis based on the dataset you previously scraped. The management has no technical background. Broadly speaking, they have two main questions:

- What are currently the most interesting insights about the Belgian real estate market?
- What variables are the most important when determining the price of a property?


## Approach
 Using Pandas for data manipulation.
 Using MatplotLib for plotting.
 Finding and understanding correlations between dataset's variables.


## The dataset

For this project, we used a Dataset of 15.000 real estate’s observations, previously scrapped by Urson during the previous project with Immo Eliza’s.

## Step 1: Data Cleaning
The cleaning phase is very important: without a good cleaning, our analysis could be badly influenced by outliers. That’s why we decided to divide the data cleaning by many small steps:

### Remove duplicates based on Property ID
A very first clean to the raw data. We were focused on dropping the duplicates based on Property ID.

### Drop rows without a price and a region
Then we decided to drop rows without a price and a region.

### Filter and removed data
We decided to filter and remove certain rows based on anomaly detection. For example, we dropped rows with FloorCount >= 20, BedroomCount > 20, or FacadeCount > 8, because it is very abnormal in real life that a house or an apartment have more than 20 floors or 20 bedrooms or 20 facades.


## Step 2: Data Analysis
### Observations and features
At the end of the cleaning phase, we had 5717 rows (observations) and 32 columns (features).

### Proportion of missing values per column
Here is the table of columns with more than 20% missing values in original dataset:

| Column | Missing percentage |
| ------------- | ------------- |
| Garden_Area | 82.00 |
| Terrace_Area | 55.72 |
| LandSurface | 53.23 |
| LandWidth | 53.23 |
| FloorCount | 40.38 |
| ConstructionYear | 32.01 |
| KitchenType | 30.81 |
| FacadeCount | 27.14 |
| StateBuilding | 22.47 |

### Columns to be deleted
We could delete these columns: Open_fire, TypeSale, PriceType, LifeAnnuitySale, Swimming_pool because only 5% of properties have an open fire, while 95% do not; less than 2% of properties have a swimming pool and only 3% of properties are furnished, indicating this is a rare feature.

The column url_scraped could be optionaly deleted but we would keep because we used it for checking listings and anomalies.

### Correlation between variables and price
Here is the correlation between different variables and the property Price (descending):

| Variable | Correlation with Price |
| ------------- | ------------- |
| LivingArea | 0.70 |
| Terrace_Area | 0.38 |
| BedroomCount | 0.34 |
| Open_fire | 0.15 |
| SwimmingPool | 0.15 |

Through the table above, we see that the variable “LivingArea” has the strongest positive correlation with the price. “Terrace_Area”, “BedroomCount”  follow with a moderate positive correlation. “Open_fire”, “SwimmingPool” also have a correlation with the price.

### Notes
For questions about qualitative and quantitative variables, how do variables themselves correlate to each other, how the number of properties are distributed according to their surface?, 5 most important variables, Least/most expensive municipalities in Belgium/Wallonia/Flanders? (_in terms of price per m², average price, and median price_), you can find the answers in the slides of presentation.
