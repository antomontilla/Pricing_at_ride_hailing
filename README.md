README

## Project: Understanding what drives prices of ride-hailing services

### Introduction and motivation
- In the era of app-based transportation services, companies like Uber and Lyft have revolutionized the traditional taxi model by implementing sophisticated technologies. 
- Through a centralized and automated system, these ride-hailing giants connect passengers with drivers in a dynamic, two-sided marketplace. 
- However, unlike conventional taxi services, the pricing strategies employed by these companies extend beyond mere distance calculations, incorporating a set of undisclosed factors.
- Central to this pricing approach is the concept of dynamic pricing - a complex algorithm that adapts rates based on various variables impacting the timing of the ride. Factors such as traffic conditions, extreme weather, and specific times of the day or week contribute to the dynamic nature of these pricing models. As Uber acknowledges, this may result in temporary price increases during peak demand periods (see [Uber Blog](https://www.uber.com/en-GB/blog/uber-dynamic-pricing/#:~:text=That%27s%20because%20of%20our%20dynamic,price%20during%20particularly%20busy%20periods.)).
- The ride-hailing companies argue that such dynamic pricing algorithms effectively address imbalances between ride supply and demand, thereby enhancing the overall experience for both riders and drivers. However, the lack of transparency surrounding the parameters and inputs of these algorithms raises questions about the fairness and understanding of the pricing mechanism.
- This project aims to unveil some of the variables influencing dynamic pricing algorithms, with a specific focus on how weather conditions and the time of day or week impact ride costs. 
- Leveraging data obtained through Uber and Lyft APIs and accessible on Kaggle ([Dataset Link](https://www.kaggle.com/datasets/ravi72munde/uber-lyft-cab-prices?select=cab_rides.csv)), we delve into a dataset comprising 693,071 rows of simulated rides with real prices. Collected in the city of Boston in November 2018 for 12 specific districts, this dataset serves as the foundation for our exploration into the intricate dynamics of ride-hailing pricing strategies.

### Objectives

1) **Examime pricing patterns.** Explore and analyse the database published in Kaggle to better understand the distribution of ride-hailing prices during the day and week.
2) **Uncover the impact of weather.** Connect this dataset with weather conditions, with the aim to explore how the weather affects ride-hailing prices.
3) **Comprehensive Exploratory Data Analysis (EDA).** Conduct a through Exploratory Data Analysis of the combined dataset. Employing statistical and visual techniques, this step seeks to uncover correlations, trends, and anomalies, laying the groundwork for subsequent modeling.
4) **Machine Learning Regression Modelling.** Utilize machine learning techniques to construct a regression model predicting ride-hailing prices based on selected features.
5) **Model Evaluation and Selection.** Compare different regression models for selecting the algorithm that best fit the dataset.
6) **Analyse Model Parameters and Conclude.** Investigate the weight and significance of each feature in the regression model. This analysis serves as compelling evidence for understanding how dynamic pricing mechanisms operate, offering valuable insights into the factors that exert the most influence on ride costs.

### Tech/framework used & links to other resources
- The project was developed using Jupyter in Python, for importing the database, looking at the relationship between the average/price per mile and other columns and building machine learning models for estimating prices.
- Jupyter notebooks can ben found in this git repository.
- Exploratory Data Analysis was complemented in a Tableau notebook ([Public Tableau Notebook](https://public.tableau.com/app/profile/antonio.montilla/viz/Ride_hiling_prices/Priceversuswind)).
- A presentation with main insights of the project can be found also in the repository.

### Main findings, caveats and further analysis.
- The aim of this project was to analyse and identify the main factors behind the pricing strategy of ride-hailing companies, using a dataset for Uber and Lyft trips provided in a Kaggle challenge.
- As shown throughout the analysis, distance is by the far the most influencing factor in the estimated price of ride-hailing services, a factor that is indeed the fundamental input that Uber identifies when disclosing how it sets its standard rates.
- Other factors that have some relevance in prices are also the type of service chosen in the App, for example if the request is for a wheelchair-accessible vehicle or for a large car (XL).
- However, the analysis also showed that the price per mile set by Uber could be incremented during periods of high demand, relative to the number of available drivers (using a dynamic pricing algorithm).
- For example, in morning rush hours, there is evidence that the average price per mile could be 15% higher relative to the average price per mile in the overall database. In afternoon rush hours or during the weekend, there is also some evidence of higher average prices. By contrast, except during very extreme circumstances, there was little evidence to suggest that weather conditions significantly affect prices.
- Overall, prices get incremented relative to standard rates only in a relatively small share of the observations (for the Lyft database, dynamic pricing took place only in 7% of total rides).
- There a number of caveats, however, to highlight in this analysis. First, and mostly, the data used in this project was taken for only 1 week in 12 districts of the city of Boston and therefore is unlikely to be representative of the overall distribution of prices set by these companies throughout the year.
- Furthermore, the data account only for simulated requested trips made through the Uber and Lyft APIs by the same user, where only very limited amount of information was able to be collected. Moreover, the fact that the trip requests were made by the same user does not allow to analyse the potential effect on prices from customer profiling.
- Given all of the above, it is very likely that other factors are indeed at play in setting prices for ride-hailing services. At the very least, further analysis will require a recollection of data using different users, for a longer period of time and involving a larger number of geographic locations.
