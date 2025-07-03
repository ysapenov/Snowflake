Lab Overview  
For those who begin to study Snowflake from scratch, it is recommended to start with “Hands-On Lab Guide for Snowflake Free Trial” that describes how to work with the main database features in the form of step-by-step guide.  
This Lab offers a high-level description of the practical task for self-directed learning.  
The target group for the Lab are DWBI engineers with experience in building Data Warehouses using other databases (Oracle, MS SQL, Teradata, etc.).  

Lab Data Set  
Data set from TPC-H benchmark (https://www.tpc.org/tpch/) is proposed for the Lab. TPC-H allows you to generate data for 8 tables. The data volume (in gigabytes) is defined by scale factor (SF). 

Lab Description  
Hands-on-lab is considered as completed if you score >= 60 points.  
(Tasks 1, 8 – 5 points each, Tasks 2, 4, 5, 6 – 10 points each, Task 3 – 30 points, Task 7 – 20 points).

1.	Database creation  
First, you need to create a separate database in Snowflake.

2.	Data loading  
In this step, you need to load Lab data set to internal (Snowflake) or external stage.  If you have an existing account in AWS/GCP/Azure cloud, external stage would be preferable. Please note that you may need some data preparation steps before loading.

3.	ELT Data Workflow  
Create two schemas in the DB you created before:  
•	CORE_DWH  
•	DATA_MART  
Develop the following automated data workflow:  
Stage -> CORE_DWH -> DATA_MART  
Data in CORE_DWH should be modeled according to 3NF (as is - no transformation). Star Schema is a target data model for DATA_MART (data should be transformed accordingly).  
The following Snowflake features should be used:  
•	Tasks  
•	Stored Procedures  
•	Tables Streams

4.	Snowflake & 3rd party tools  
When the data is loaded to DATA_MART schema, connect Snowflake as a data source from any BI tool (Tableau, PowerBI, Qlik Sense, etc.) and create a simple dashboard.
Also, try connecting to Snowflake from any SQL editor (e.g. DBeaver).

5.	Snowflake SQL  
•	Create several warehouses of different sizes and compare their performance;  
•	Test how Snowflake leverages different types of cashes;  
•	Rewrite a couple of queries to execute on Start Schema data model and compare performance (3NF vs Star Schema);  
•	Execute queries using SnowSQL (CLI Client).

6.	Other Snowflake features  
Learn and test other interesting Snowflake features:  
•	Object Cloning;  
•	Time Travel;  
•	Data Sharing - share your DATA_MART schema with a colleague who helps you with this Lab.

7.	Snowpipe  
Automated incremental data loading using Snowpipe. Split lineitem & order files into several parts and simulate their sequential loading to stage buckets.

8.	Additional tasks  
Connect your Snowflake account with partner applications available for a free trial (e.g. Fivetran, Periscope Data, Matillion in Partner Connect menu). Explore how selected tools work.