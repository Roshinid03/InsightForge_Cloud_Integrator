GOAL
My main goal of this project is to transform my data in GitHub to Azure Cloud, then connect the cloud data warehouse to PowerBI to create a dashboard.
PROJECT OVERVIEW
I have considered Tokyo Olympics Dataset from Kaggle. The dataset was added to GitHub account and then data pipelines to transfer data from GitHub to Azure Storage Accounts were created using Azure Data Factory. Created an App Permission and gave access to Databricks to load the data from storage account and preprocessed and cleaned the data. After the data preprocessing, loaded back the data into storage account. Created a Azure Synapse Analytics workspace and connected it to Power BI to create the dashboard using the final data.
SERVICES USED
 GitHub, Azure Storage Accounts, Azure Data Factory, Databricks, Azure App Registrations, Azure Synapse Analytics and Power BI.
STEPS
1.	Downloaded the dataset from Kaggle and loaded the dataset to the GitHub repository.
2.	Created a Resource Group on Azure Cloud.
3.	Created a Storage account in Azure cloud with two folders raw-data and transformed-data.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/84d6ed67-fccc-4586-bc57-436e831a0f22)
4.  Created a Data Factory studio and launched it. Created data pipelines to load data from HTTP source to raw-data folder of Storage Account.
   ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/668a251c-229d-4eb7-a003-abaf0628934a)
   ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/f97f3bda-7398-4f2b-bafd-f8661b6bab44)
5.	Created an App Registration to authenticate Data Bricks to access the storage account to load the raw data.
   ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/aaf3cb87-727c-4679-a88d-8ff1b9e36d47)
6.	Created a DataBricks studio and launched it. Loaded the data from Storage Account by mounting the dataset.
   ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/3456f779-c582-4026-9713-f0d53e3e8de7)
7.	 Preprocessed the data loaded in Databricks using pyspark. Considering the missing values, changing the datatype of the data when required, loaded back the data into transformed-data folder of azure storage accounts.

   Importing pyspark libraries                              
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/7ae5eb7b-9c8b-44ae-9c92-cf204744bf07)
   Creating the authentication and creating the connection between Databricks and storage account. Mounting the raw data from storage account to data bricks.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/5119215e-31e8-458d-840b-96f92542065e)
    Displaying the path of list of folders in that particular container.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/32e5ddfc-2490-4256-9039-8572111a8954)
    Type Casting the datatype of the data in files using option.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/e8212979-f48f-4f5c-bd7e-5c1db7100814)
    Displaying the data of entriesgender file.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/4943d88b-e96f-444d-a700-493f2b64e67e)
    Displaying the schema of entriesgender file.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/b5de8a54-199c-43e2-9306-8d9d9581f6e9)
    Displaying the Schema of medals file.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/64ef9d6c-3b06-4da6-b193-4e44c9a9a889)
    Using a query to convert the datatype (TypeCasting) 
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/ec439a5c-c4de-4909-90c8-57724aead60b)
    Loading the data to Transformed folder of Azure storage account.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/2b8bb820-98bf-438d-b233-b25c799f0e8e)
    Files loaded in Transformed folder of Azure Storage Account.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/b27c570b-b76a-406a-946f-706f461e5ed7)
8.	Created an Azure Synapse Analytics studio and loaded the data to access using SQL Scripts.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/cea5b130-2215-4c53-9068-fbf87df9741b)
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/f1071bca-e216-4ccc-acfc-60a19041c40b)
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/14842ea2-c9a6-48ea-87fd-b2dbab45a46b)
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/430ab4a8-0a4f-42a2-aaa6-dcfaee1ac872)
9.	Created dashboard in Power BI in Azure Synapse Analytics Studio.
    ![image](https://github.com/Roshinid03/InsightForge_Cloud_Integrator/assets/150306520/9e6d03da-e267-4e96-b488-d7511db83193)






