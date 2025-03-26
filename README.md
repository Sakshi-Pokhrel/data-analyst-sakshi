# data-analyst-sakshi
# Project 1: AWS Analysis for University Canada West (Human Resource Department)
We created an AWS project for University Canada West and the area I was working for was for the occupational health and services procedure under Human Resource Department. The three data that I selected for it were
- regulation list
- worker list
- workplace list
I worked as a data team for UCW account and was able to achieve vaious milestones in it. Now, I will be discussing various services we used in AWS and that deliverables we were able to generate from it.

**1. Exploratory Data Analysis**

**Project Description:** Exploratory Data Analysis on UCW's Occupational health and Services procedure
 
**Objective**: The main objective was to store, clean, and summarize our data so that it can be used for analysis. This way, we can understand the data and check for any 
     inconsistencies along the way.

**Dataset**: We are working with three data set as mentioned above which were regulation list, workers list, and workplace list. The regulation list included details like name of the regulation, the regulation ID, who is responsible for it, when should it be followed, if trainings are provided for it or not. For workers list, their name, age, location, years of experience, any certification are included. In case of workplace list, location, assigned worker, time, recordins of hazards and so on. So these were the type of data set we were working with.

**Methodology**: Firstly, we had to ingest the data from the webserver and store it in the bucket as a raw file. After that, we had to clean to data to transform it before summarizing them for any further analysis.

**Tools**: To ingest and store the data, we used S3 services by creating a bucket in them and for cleaning and profiling the data, we used AWS Glue DataBrew services where we created jobs for cleaning and profiling them.

**Deliverables**: we were able to achieve cleaned, transformed data set which could be used for further analysis. These data could also be summarized and thus generate queries after that.

![Data Ingestion from Web Server](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/draw.io%20file%202.png?raw=true) 
![Data Transformed](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/drawio.2.png?raw=true)


**2. Descriptive Analysis**

**Project Description**: Doing descriptive analysis on UCW's occupational health and services procedure.

**Objective**: Basically, we did do descriptive analysis in this project to understand business queries and figure out what results were generated. This helps in understanding business related questions, gives insights to the analytics.

**Dataset:** Again, we used the same dataset of occupational health procedures. We tried to generate atleast three of those queries using the data set that we had.

**Methodology:** In order to be able to generate those business queries, firstly, we had to summarize our transformed data and curate it. we had to create pipelines and store it in a centralized data calaog after which we were able to write SQL and generate our business related queries.

**Tools:** Firstly, in order to create a pipeline, we used visual ETL feature from AWS glue service and once pipeline was created, we use crawler and centralized our data in data catalog. After that, we used Amazon Athena services where we could write SQL code and generate queries.

**Deliverables**: We were able to catalog our data and get answer to three of our business queries. It helped in understanding the average number of employees, maximum square footage of safety that needed to be maintained and also minumum salary wage that is been given to the employees.

![Business query 1](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/ss4.png?raw=true)
![Business query 2](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/ss5.png?raw=true)
![Business query 3](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/ss6.png?raw=true)

3. Data Wrangling

**Project Description**: Doing data wrangling on UCW's occupational health and services procedure.

**Objective**: The main objective of data wrangling is to handling missing values, correcting errors, and restructuring data to make it more accessible and meaningful. It means we need to profile and clean them for better analysis.

**Dataset:** Again, we used the same dataset of occupational health procedures. We shall be wrangling data for three data set that we have which are regulation list, workers list and workplace list. 

**Methodology:** In order to be able to wrangle it, firstly, we had to extract data from the raw data set, then we created a job to profile them and then again we had to run a job to clean them and again store those transformed data in another bucket.

**Tools:** The tools that we use to profile and clean them is called AWS Glue DataBrew. We create a job to profile them here and again in the same DataBrew, we could clean them and store them in another bucket. So, for storage we need S3 service.

**Deliverables**: We were able to provide clean, profiled and transformed data set which had no missing, invalid or incorrect values. The data now are ready for further summarization.

![Data profiling 1](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/regulation%20list%20profiling%202.png?raw=true)
![Data profiling 2](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/workers%20list%20profiling%202.png?raw=true)
![Data profilimg 3](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/workplace%20list%20profilig%202.png?raw=true)
![Data cleaning all](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/Cleaning%20all%203%20jobs.png?raw=true)

4. Data Quality Checking

**Project Description**: Doing quality check on UCW's occupational health and services procedure.

**Objective**: The main objective of data quality check is to figure out and see how many data pass the quality check so that they can be segregated into failed bucket or onto pass bucket

**Dataset:** Here, we use semi-structured JSON file which contains our data set of regulation list, workers list and workplace list. 

**Methodology:** In order to check the quality of the dataset, firstly, we had to extract data from the semi-structured dataset bucket, then we created a pipeline and used conditional routing to check weather the data passes the quality in terms of completeness, uniqueness and freshness. Based on it, data could be separated into quality passed or quality failed.

**Tools:** The tools that we use in this case are S3 firstly to store the semi-structured data and again store them back into the bucekts after testing its quality. We used Visual ETL feature from AWS Glue to create the pipeline and do conditional routing.

**Deliverables**: We were able to separate our data into two buckets, the first one had data set which passed the quality and the second bucket had dataset which failed the quality.

![Data Pipeline](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/CA8-1.png?raw=true)
![Quality check 1](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/CA8-2.png?raw=true)
![Quality check 2](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/CA8-3.png?raw=true)

5. Data Monitoring
   
**Project Description**: Doing data monitoring on UCW's occupational health and services procedure.

**Objective**: The main objective of data monitoring is to optimize the cost of using resources in AWS. Along with that, it is also important to keep track of the activities in the console anywhere from user activity to the data team activity.

**Dataset:** Here, we used monitoring on all the services that had been used. Using maximum would increase cost accordingly.

**Methodology:** In order to monitor our services, we create dashboard for different metrics and services and generate a threshold beyond which we would be notified by again creating an alarm which helps with notification.

**Tools:** The tools that we use in this case are CloudWatch and CloudTrail. CloudWatch helps with monitoring and CloudTrail helps with tracking activities.

**Deliverables**: We are able to identify the activities and see what is being done. Along with that, we are able to monitor usage to optimize the cost.

![Cloud Watch](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/CA9-1.png?raw=true)
![Cloud Trail](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/CA9-2.png?raw=true)
   
# Project 2: AWS Analysis for City of Vancouver (Bikeways)
   
We did an AWS Analysis for City of Vancouver- Bikeways procedures where we analysed those data to generate queries with it. There are varipus services and features we used to make it ready for future analysis.

**1. Exploratory Data Analysis**

**Project Description:** Exploratory Data Analysis on City of vancouver bikeways
 
**Objective**: The main objective was to store, clean, and summarize our data so that it can be used for analysis. This way, we can understand the data and check for any 
     inconsistencies along the way.

**Dataset**: We are working with bikeways dataset where we have bikr routes, street name, bikeways type, speed limit, vehicle direction, and so on.

**Methodology**: Firstly, we had to ingest the data from the webserver and store it in the bucket as a raw file. After that, we had to clean to data to transform it before summarizing them for any further analysis.

**Tools**: To ingest and store the data, we used S3 services by creating a bucket in them and for cleaning and profiling the data, we used AWS Glue DataBrew services where we created jobs for cleaning and profiling them.

**Deliverables**: we were able to achieve cleaned, transformed data set which could be used for further analysis. These data could also be summarized and thus generate queries after that.

![Data Ingestion from Web Server]() 
![Data Transformed]()


**2. Descriptive Analysis**

**Project Description**: Doing descriptive analysis on UCW's occupational health and services procedure.

**Objective**: Basically, we did do descriptive analysis in this project to understand business queries and figure out what results were generated. This helps in understanding business related questions, gives insights to the analytics.

**Dataset:** Again, we used the same dataset of occupational health procedures. We tried to generate atleast three of those queries using the data set that we had.

**Methodology:** In order to be able to generate those business queries, firstly, we had to summarize our transformed data and curate it. we had to create pipelines and store it in a centralized data calaog after which we were able to write SQL and generate our business related queries.

**Tools:** Firstly, in order to create a pipeline, we used visual ETL feature from AWS glue service and once pipeline was created, we use crawler and centralized our data in data catalog. After that, we used Amazon Athena services where we could write SQL code and generate queries.

**Deliverables**: We were able to catalog our data and get answer to three of our business queries. It helped in understanding the average number of employees, maximum square footage of safety that needed to be maintained and also minumum salary wage that is been given to the employees.

![Business query 1](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/ss4.png?raw=true)
![Business query 2](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/ss5.png?raw=true)
![Business query 3](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/ss6.png?raw=true)

3. Data Wrangling

**Project Description**: Doing data wrangling on UCW's occupational health and services procedure.

**Objective**: The main objective of data wrangling is to handling missing values, correcting errors, and restructuring data to make it more accessible and meaningful. It means we need to profile and clean them for better analysis.

**Dataset:** Again, we used the same dataset of occupational health procedures. We shall be wrangling data for three data set that we have which are regulation list, workers list and workplace list. 

**Methodology:** In order to be able to wrangle it, firstly, we had to extract data from the raw data set, then we created a job to profile them and then again we had to run a job to clean them and again store those transformed data in another bucket.

**Tools:** The tools that we use to profile and clean them is called AWS Glue DataBrew. We create a job to profile them here and again in the same DataBrew, we could clean them and store them in another bucket. So, for storage we need S3 service.

**Deliverables**: We were able to provide clean, profiled and transformed data set which had no missing, invalid or incorrect values. The data now are ready for further summarization.

![Data profiling 1](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/regulation%20list%20profiling%202.png?raw=true)
![Data profiling 2](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/workers%20list%20profiling%202.png?raw=true)
![Data profilimg 3](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/workplace%20list%20profilig%202.png?raw=true)
![Data cleaning all](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/Cleaning%20all%203%20jobs.png?raw=true)

4. Data Quality Checking

**Project Description**: Doing quality check on City of Vancouver's bikeways procedure.

**Objective**: The main objective of data quality check is to figure out and see how many data pass the quality check so that they can be segregated into failed bucket or onto pass bucket

**Dataset:** Here, we use semi-structured JSON file which contains our data set for the bikeways. 

**Methodology:** In order to check the quality of the dataset, firstly, we had to extract data from the semi-structured dataset bucket, then we created a pipeline and used conditional routing to check weather the data passes the quality in terms of completeness, uniqueness and freshness. Based on it, data could be separated into quality passed or quality failed.

**Tools:** The tools that we use in this case are S3 firstly to store the semi-structured data and again store them back into the bucekts after testing its quality. We used Visual ETL feature from AWS Glue to create the pipeline and do conditional routing.

**Deliverables**: We were able to separate our data into two buckets, the first one had data set which passed the quality and the second bucket had dataset which failed the quality.



