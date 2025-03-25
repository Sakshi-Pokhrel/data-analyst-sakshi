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

![Data Profiling and Cleaning](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/drawio.2.png?raw=true)

![AWS Data Cleaning](https://github.com/Sakshi-Pokhrel/data-analyst-sakshi/blob/main/Cleaning%20all%203%20jobs.png?raw=true)



