# Movies-ETL

## Purpose
The purpose of this excercise was to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables (ETL). A function that takes in the three files —- Wikipedia data, Kaggle metadata, and the MovieLens rating data -- was created and then cleaned and ultimately added to a PostgreSQL database.

## Resources
### Data Tools and Resources
* Python 3.9
* Anaconda 4.8.5
* Pandas
* Jupyter Notebook 6.1.4
* PostgreSQL 11
* `Resources/ratings.csv`
* `Resources/movies_metadata.csv`
* `Resources/wikipedia-movies.json`

## Results
### ETL Function Test (`ETL_function_test.ipynb`)
* Created a function to read in the three files.
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/etl_function.png)

* Turned the 3 files into a DataFrame
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/deliverable1-1.png)

![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/deliverable1-2.png)

![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/deliverable1-3.png)

### Processed the Wiki Data. (`ETL_clean_wiki_movies.ipynb`)
* Processed the wiki data to remove unecessary columns and changed data types
* changed certain data types from stings to float types
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/wiki_movies_df.png)
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/wiki_movie_columns.png)

### Processed the Kaggle Data (`ETL_clean_kaggle_data.ipynb`)
* Processed the kaggle data to remove unnecessary columns, filled in missing data and change data types
* Merged wiki movies and kaggle data to form `movies_df` DataFrame. 
* Merged ratings with movies_df.
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/movies_with_ratings.png)

### Load to PostgreSQL (`ETL_create_database.ipynb`)
* Added the movies_df DataFrame and MovieLens rating CSV data to a SQL database.
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/ratings_to_sql_export.png)

* Counted the number of rows for both movies_df and rating.csv in PostgreSQL.
![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/movies_query.png)

![](https://github.com/jaredcclarke/Movies-ETL/blob/main/Resources/Resources/ratings_query.png)
