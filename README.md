# Sentiment Analysis of Fabric DE Project of NewsData

![Slide1](https://github.com/Abdur-RasheedAde/Fabric_DE_Project_of_News_with_Sentiment_Analysis/blob/main/News%20Sentiment%20Analysis.png)

##  Project Summary
This is a Fabric Data Engineering project including Data Science sentiment analysis on a news data. The project ingested data using a datapipeline built in DataFractory to load data from (newsdata.io), an open source news repository which has free API keys. The data is stored as a json file in Fabric LakeHouse. The ETL process and Sentiment analysis were done using Pyspark in a jupyter notebook while Power BI was used to Visualize the final clean data. An alert was also created in PowerBI for one of the visuals using Reflex Activator  

## Data Source: 
Datasource: News data were loaded from https://newsdata.io/search-news with the appropriate API keys

## DE Technical Skills:
+ Data Ingestion
+ Data Pipeline: Datafactory, increamental load, schedule refresh
+ Fabric Data Storage: json, Lake House
+ Data Science: Sentiment Analysis, ML Model 
+ Data Warehousing; Analytics Reporting
+ Extract, Transform and Load (ETL) process
+ Some Power BI Data Visualization technical skills (Documentation, Data Gathering, Power Query, Data Modelling, Report Design, Data Analysis Expression (DAX), Page Navigation and Button, Business and Analytics Reporting, Performance Optimization, Deployment and Power BI Service, Scalability)
+ Continuous Improvement
  
## Data Engineering Process
1. Creation of Workspace and Lake House: A new workspace was created to host all fabric items (Notebooks, lakehouse, pipeline, Reports, Dataset...) needed for this project. Thereafter, a Lakehouse known as News_Lake was then created in the workspace to stores all files and data table.
2. Data Ingestion: Data was ingested from this 👉 news website (newsdata.io). A paramitarized data pipeline was built with Fabric Data Factory to connect through a RESTAPI using the appropriate API keys. The data comes in a json file and stored as File in LakeHouse.
3. Data Transformation: The whole Extract Transform and Load (ETL) Process was done in a Jupyter Notebook in the Lakehouse with the use of pyspark. The Transformation includes and not limited to:
-  Explosion of json data
-  Conversion of json file to a list and json dictionary
-  Exception handling... 
4. Data Warehousing - Incremental Load: Inorder to avoid duplicate of data and table as well as lost of data, a **Type 1 SQL Merger Data Warehousing Incremental Load** was adopted to load latest news data to the existing table in the Datawarehouse (Lakehouse).\
The clean and well structured data was loaded to a LakeTable 
-  [View ETL codes here](https://github.com/Abdur-RasheedAde/Fabric_DE_Project_of_News_with_Sentiment_Analysis/blob/main/ETL_Process_of_News.ipynb)
5. Data Science Sentiment Analysis with ML Model: The new and appended table in the Lakehouse was loaded through a jupyter notebook while a Synapse ML Model was explored to perform sentiment analysis to categorise the description column. Data then loaded again into another table in the Lakehouse while maintaining the same Type 1 Data warehouse Incremental Load.\
[View Sentiment Analysis codes here](https://github.com/Abdur-RasheedAde/Fabric_DE_Project_of_News_with_Sentiment_Analysis/blob/main/Sentiment_Analysis.ipynb)
6. Schedule Refresh: Since the news data is live, there is need to schedule it's refresh every morning at 9am in Data Factory. This refresh covers the data Ingestion (pipeline), ETL process (notebook) and Sentiment Analysis (notebook)
The refresh schedule is shown here 👇
![Refresh](https://github.com/Abdur-RasheedAde/Fabric_DE_Project_of_News_with_Sentiment_Analysis/blob/main/Fabric_News_ingestion_pipeline.PNG)
7. Visualization and Report: A Power BI Report was built directly from the loaded Sentiment Analysis Table in LakeHouse with KPIs ranging from counts of positive, negative, mixed and neutral news as well as their corresponding percebtage.
The Power BI Report as well as it's model was hosted within the workspace.
 
## KPI Building 
While building the visualization, the following KPIs were considered;
1. Count of each review (positive, negative, neutral and mixed
2. Percentage of each review type
3. Total Review
4. Review by Country
5. Review by category...

## Report Design and Visualization
+ The Report Canvas was designed in Power Point and imported to PowerBI as canvas background.
+ Only 2 pages were created, the Home page and KPI page.
+ A sample of the Home page in Power Point shall be uploaded soon.
 
Link to download PowerBI PDF Report shall also be uploaed soon.

## Data Activator: 
A reflex Data Activator alert was created for the Negative review card Visuals which sends daily report via Outlook if the review count is > 10.


## Conclusions 
1. Microsoft Fabric is a one-stop shop that replicate all Azure Data Services (known as items in Fabric) in one space. These items include DataFactory, Power BI, LakeHouse, Notebooks, Pipeline and so on. 
2. It can iterract with all internal and external data sources like Azure, AWS, GCP, Dataverse and coud services like Databricks, Snowflake and others.
3. It extensively supports SQL, Python, Scala and java Programming Languages
4. It is awesome for Data warehousing and ETL process and visualization.

Thanks for taking time to go through this report! and I am open to collaborate with you on any Data Engineering projects exploring Fabric, Azure data services or other cloud big data platforms especially Databricks, Snowflake, AWS and GCP, you can always reach me on adeoyerasheed30@gmail.com Ciao 🤝
