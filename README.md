# DB_assignment3
SPA - Study points assigment for Database

## Neo4J

### 1. Explore the data and formulate considerations about a hosting database.
We chose to do minimal cleaning of the data, from previous database project in MongoDB where we cleaned the data in Jupyter. 

### 2. Design and develop proper database structure of the requested type.
From each of the former databases, we by default have the idea for structuring the Neo4J database. 


### 3. Ingest the data into the database, include pre-processing of it, if necessary.
We pre-processed the data slightly, to make sure all objects in the database have the same field called 'Organisation' instead of 'Organization' or 'Account' etc. We did the same with 'City', 'C40 City' and 'Organisation Number' and more. 

### 4. Design and develop operations for maintenance of the database.
For maintenance we will use backups and restore tools to ensure data integrity, we will use the build-in tools '**neo4j-admin backup**' and '**neo4j-admin restore**'.

### 5. Formulate ten relevant questions for extracting information from the database, design and develop database functionality for implementing the information extraction (for the relevance consult the instructor).
1. Is there a correlation between population and total emissions?
2. From 2016 to 2017, has there been a reduction in base emissions?
3. From 2016 to 2017, what change has there been in target emission?
4. Is there a difference in the target reduction emissions based on whether or not the city is a member of C40 or GCoM?
5. What difference is there between each region and their target emission?
6. Which organization plans to reduce the most in %?
7. For each country, how many cities in that country is represented in the data?
8. How many countries are represented in the data?
9. How many have a desired target emission without a base emission?
10. What is the most commeon sector?

Answers for the questions can be found in the Jupyter, in the buttom we have answered all the questions and also on our frontend.


### 6. Design and implement a model for scaling the database, considering ACID and/or CAP theorem rules.
Neo4J adheres to ACID (Atomicity, Consistency, Isolation, Durability) properties for transactions within a single instance. 

For CAP, Neo4j's architecture is designed to provide strong consistency (C) and high availability (A) in a distributed environment. though achieving full partition tolerance (P) may require trade-offs in certain scenarios.

### 7. Validate and test all database operations.
We tested it with the aggregation pipelines and by using CRUD operations on some data.

### 8. Evaluate the database’s performance and suggest measures for improving it.
* Not really needed, as the amount of data is still too low to need these measures/optimizatioins (only at most some 2000 rows in a table)
* Potentially something to look into, if one wants to scale the database further (say hypothetically, the database were to be updated yearly, how much data would be added?)


### 9. Document your work, describing the product and the process. Apply graphical notation (diagrams), when it is possible.
We used Jupyter Notebook to create some a database connection to Neo4J, in the jupyter file, we started with adding the materials from the previous assigment (SPA2), we checked for nulls as Neo4J cant handle NaN/Null, so we renamed them **None**. From there we connected to the Neo4J database to input our data into it and to answer our questions. 

### 10. Formulate conclusions and recommendations.

Answers for the questions can be found in the buttom of the jupyter file.

## Frontend code
Simple Node.js frontend

Github [link](https://github.com/Gruppe-H/db2_frontend)
