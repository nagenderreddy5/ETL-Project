# ETL-Project: Netflix Subscriber and Revenue data
In this Project, we found data from Kaggle about Netflix Titles, Revenue and Subscribers. To look closer at this data, we used Pandas in Jupyter Notebook to filter the CSVs and join them. We then used PostgreSQL to take another look at the data and how they compare.

## Extract
### Data Sources
Kaggle:
Netflix Originals (https://www.kaggle.com/abhimanyudasarwar/netflix-originals)
Netflix Subscribers and Revenue (https://www.kaggle.com/pariaagharabi/netflix2020)

## Transform
### Dependencies
We first determined the dependencies in the Jupyter Notebook:
-Pandas
-Sqlalchemy
-DateTime

Once Dependencies were set, we read in the CSVs. To transform the Netflix Originals data, we needed to filter the tables to only reflect the usable columns of Title, Genre and Premiere.

In order to join all of the tables, we needed a common column to join on. This means we needed to adjust the 'Premiere' column to be in the same format as the 'Year' column in the other CSVs. To do this, we used the DateTime variable to make a new column to reflect the similar format. With the new column, we then could remove the old Premiere column.

To keep the data simplified, we filtered the Revenue and Subscriber data to only reflect the United States and Canada Area. 

We then were able to merge the tables into one. And then to ensure the entire table was usable, we got rid of any NaN rows.

## Load
Now that the tables are clean, we created tables and imported the clean data into PostgreSQL. Here we can continue to look at the comparison of data.
