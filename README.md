# Predicting Footwear Prices

## Introduction & Project formulation

All data analysis begins with some data. I chose a data source applicable to a standard buisness problem from Kaggle here: https://www.kaggle.com/datafiniti/womens-shoes-prices. 

I started by reading the Kaggle description along with the schema here https://developer.datafiniti.co/docs/product-data-schema. The data consists of rows of shoe listings and columns of associated prices and other features and is **only a small sample** (10,000 rows) of all Women's shoe listings in the market. What is really missing from this dataset are more in direct target metrics like how many units were sold and how many times the page was viewed, which are only factors known by the retailer and the brand of a shoe.

#### How could creating a model for this dataset and analysis improve a product?
My plan is to create a machine learning derived function that predicts the prices of future listings. This could be useful in a business environment where a shoe has been designed and is planning on being distributed to retailers but the MSRP is not yet set. Or it could be used as a tool for designers to better test & understand the macro factors that will make their shoes more valuable when pitching to retailers. Note that I have not designed this as a causal model--an important distinction sometimes ignored by data scientists and analysts. 

Using Spark for a task like this <b>is overkill</b> because the size of the dataset (26 mb) can easily be fit into the memory of most computers. However, using such a small database allowed me to upload the data and process via the databricks servers quickly despite having tiny upload bandwidth (and this is an example project/reference).

Unlike many other examples of Spark being used for analysis, I have intentionally NOT converted to a Pandas dataframe—so all the concepts, algorithms, and analysis can be scaled to a larger database with ease.

You can find the hosted notebook here: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/5379433019465152/194281337381761/5498857450185350/latest.html

### To do:
#### 1. Include predictive functionality
#### 2. Implement pyspark's Pipeline 
#### 3. Code SVD for PySpark DataFrame API (based on PCA)
