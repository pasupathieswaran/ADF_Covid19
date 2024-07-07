## Covid Data Pipeline -Azure Data Factory

In this project, I developed an end-to-end data processing solution to handle COVID-19 data. Here's a detailed breakdown of the processes and technologies involved:

#### Data Ingestion:

* I collected COVID-19 data from various sources, including HTTP endpoints and Azure Blob Storage.
* This data was ingested into Azure Data Lake Storage Gen2 using Azure Data Factory (ADF), ensuring scalable and secure data storage.

#### Data Transformation with Azure Data Factory:

* Using ADF's Data Flows, I performed complex transformations on the ingested data. Data Flows provide a graphical interface to design data transformation logic, which runs on Spark clusters, allowing for high performance and scalability.
* After transformation, the data was loaded back into Azure Data Lake Storage Gen2.

#### Data Transformation with Databricks:

* I also utilized Databricks Notebook Activity within ADF to perform additional transformations. Databricks provides an interactive workspace for data scientists and engineers to collaborate on data analytics projects.
* These transformations were again loaded into Azure Data Lake Storage Gen2, ensuring all transformed data was centrally stored.

#### Data Loading for Reporting:

* The final step involved loading the transformed data from Azure Data Lake Storage Gen2 into Azure SQL Database using ADF.
* This allowed the data to be readily available for reporting and visualization purposes using PowerBI, facilitating easy access to insights and analytics.

#### Scheduling with Triggers:

* I used triggers in Azure Data Factory to schedule the data pipelines. This automated the workflow, ensuring data ingestion, transformation, and loading occurred at predefined intervals without manual intervention.

#### Monitoring and Logging:

* To ensure the data pipelines operated smoothly, I monitored them using ADF's built-in monitoring capabilities, Azure Monitor, and Log Analytics. This setup provided comprehensive insights into pipeline performance and helped quickly identify and resolve issues.

#### CI/CD Pipelines with Azure DevOps:

* I created Continuous Integration and Continuous Deployment (CI/CD) pipelines in Azure DevOps to manage the release of ADF pipelines to higher environments, such as testing and production.
* This streamlined the development process, ensuring that changes could be deployed consistently and reliably.

Overall, this project showcased a robust data engineering workflow using Azure's suite of tools, enabling efficient data processing, transformation, and reporting.






