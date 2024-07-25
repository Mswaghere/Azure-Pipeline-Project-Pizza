
# Azure-Project (SQL - Azure Data Factory - DataBricks - PySpark - Power BI)

# Business Requirements 
We have data available in the SQL server and we need to move it to cloud storage. Build a pipeline to transfer data and run daily. Connect it with a DataBricks account, and also create an aggregated table for reporting with business-related KPIs. Build a dashboard to understand the data and make business decisions. 

# Flow of a Project
![Untitled Diagram drawio](https://github.com/user-attachments/assets/b10f4fb1-01b8-406a-87f2-eaaec36016d1)

# Step-By-Step Process 

Step 1: Set Up Azure Data Factory
Created an Azure Data Factory Instance.
Created a linked service for your SQL Server to connect to the data source.
Created another linked service for Azure Blob Storage to define where the data will be moved.

Step 2: Build the Data Pipeline
Created a Pipeline.
Used the Copy Data activity to define the data transfer from SQL Server to Azure Storage.
Set the source dataset to your SQL Server-linked service.
Set the destination dataset to your Azure Blob Storage linked service.
![Screenshot_20240725_141350](https://github.com/user-attachments/assets/b24f110f-7347-471a-9ec3-9729dda61e86)


Step 3: Schedule the Pipeline
Created a Schedule Trigger.
Specified the start time(daily), and time zone settings to ensure it runs at the desired time.

Step 4: Connect to Databricks
Created a Databricks Workspace.
Created a Notebook.
Used PySpark to read the data from Azure Blob Storage.
Aggregate Data Using PySpark:
Wrote PySpark code to perform transformations and created an aggregated table according to KPIs.
![Screenshot_20240725_141648](https://github.com/user-attachments/assets/84897a0c-71a5-42cc-a7e1-5a109a3e0480)
![Screenshot_20240725_141717](https://github.com/user-attachments/assets/d445d8e9-60f4-48d2-ab3d-f83ef679ecb6)



Step 5: Created a Power BI Dashboard
Connected Power BI to DataBricks Account.
Created a Dashboard according to the business requirements.
![Screenshot_20240725_142028](https://github.com/user-attachments/assets/57ceb4b3-edb6-41a5-9fbe-19ceda2b4308)


# Summary of Project Flow
Data Transfer: SQL Server → Azure Data Factory → Azure Blob Storage
Data Processing: Azure Blob Storage → Databricks (using PySpark, Spark SQL)
Reporting: Databricks → Power BI for visualization and business insights
