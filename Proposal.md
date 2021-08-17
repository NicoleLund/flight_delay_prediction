## Problem
What flight routes experience the smallest delay times from TUS (Tucson)?

## Tasks
* Nicole, Github management
* Tarak, CSV storage - AWS
    * Input files downloaded from Kaggle
        * 2017 data for Machine Learning model training
        * 2018 data for predictions
    * Output files from Data Wrangling
        * Test and see if Tableau public can upload data directly from AWS
* Tarak, Data Wrangling - Jupyter Notebook(s), Python, Pandas
    * Restrict to TUS origin
    * Convert date to day of the week
    ```python
    df.withColumn("input_timestamp",
    to_timestamp(col("input_timestamp")))
    .withColumn("week_day_number", date_format(col("input_timestamp"), "u"))
    .withColumn("week_day_abb", date_format(col("input_timestamp"), "E"))
    .show(false)
    ```
* Nicole, Pre-machine learning - Google colab or Jupyter Notebook?
    * Input needs to be uncorrelated
        * Logical assessment
        * Cross-correlation matrices?
* Nicole, Machine Learning - Google colab pyspark
    * Predict delay time
* Everyone, Visualization - Tableau
    * 2018 predicted vs actual delays
    * ???
* Amber, Host application on Github pages
    * Embed tableau dashboard into a webpage?
    
# Resources   
airport_codes.csv from http://transportation.gov/

https://datahub.io/core/airport-codes#resource-airport-codes

https://san-wang.github.io/blog/Embed-Tableau-dashboard-into-github-page-post/