# Migrate Looker (self-service BI tool) from Hive (Databricks) to Snowflake

* [Project](#project)  
  * [Situation](#situation)  
  * [Task](#task)  
  * [Action](#action)  
  * [Result](#result)  
    * [Learnings](##learnings) 

# Project 
## Situation 

The Data Platform team is responsible for providing the company with quick access to data. To improve this experience, at the beginning of 2020, the team conducted an analysis to choose and migrate our Data Warehouse in Hive to a new and more robust platform. After an extensive evaluation of the most relevant players in the market, our team chose Snowflake for its simplicity, cost, and performance.

migrate all of our Looker projects from an Apache Spark/Hive connection (Databricks) to Snowflake.

![Data Platform Architecture, 2019](projects/pictures/dp-architecture.png)

**Challenges we faced with the existing setup**
* Looker query performance was slow with Spark
* Increased resources for manual cluster management on Databricks for Looker workload in order to improve performance -> more costs 
* No indexing in Hive/Spark SQL, partitioning requires engineering times and achieved limited results 
* Lacking classic RDBMS features (Auditing, Access Control, etc.)


The main goal with the database migration was to improve the query performance and decrease the average query time. There were other reasons why we decided to use Snowflake as our reports querying engine instead of Spark:

* Data caching for repetitive queries
* Auditing (table and database usage (check Snowflake docs), who queried what and when) & Access control (user management with roles)
* Maintenance overhead with manual cluster management on Databricks for the Looker workload to improve performance
* Need of manual partitioning of the datasets, yet the most effective partition pruning is still not guaranteed

## Task 

The task was to move all tables 

## Action 

## Result
### Learnings
