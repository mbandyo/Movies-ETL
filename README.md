# Movies-ETL
This project maps an end to end process to extract, scrub and load data into a database to be used for anlysis purposes.
Specifically this process sets up a databse with movie details from recent past to facilitae analysis of popularity trends, revenues and other related datapoints. The challenge is that the various data sources may involve duplicate, incomplete and/or conflicting data. One major challenge is to make an informed decision about the final data. Specific steps are as follows:
*	Extract movie data from Wikipedia movie, Kaggle Metadata and Movielens rating data.
*	Inspect the data and make decisions on data cleaning strategy
* Finalize cleaned data
*	Load data to a relational database for use in analysis

## ETL Process
Initial pass through Wikipedia and Kaggle data reveal a number of duplicate records and differing dimensions of data points. Decisions were made to merge columns that held same information (e.g. director and directed by were separate keys holding same information). The final dataset caontained only one of these after dropping null values. Similar decisions were made for every column retained in the final data. Movielens data was relatively clean and were imported with little manipulations. Hoewever, this dataset was extremely large and very granular. The data was aggregated and a more managable dataset was created for analysis.
### Summary
The resulting dataset was smaller, but reasonable size for required analysis, clean and easier to access and use. Also relational database can ensure some data integrity proving crediblity to analysis and conclusion thereof.

