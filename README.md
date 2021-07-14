 awsdataengineering
This repository is for the AWS Data Engineering Concepts.

 This repository is created when learning the Udemy Course "Master serverless analytics with AWS Glue, QuickSight, Athena, & Redshift Spectrum (includes preview features with labs)"


AWS Services Used
Glue
Athena
Redshift Spectrum
Quicksight

Serverless Analytics Basics
Serverless Computing
    Data Lake
        AWS Components
            Architetcure


 This is for the building a serverless Analytics architecture in AWS.

 Serverless Basics

 Section I
Amazon S3 - Test Data Setup.
Create Buckets --> Upload Data --> Configure Storage Analytics

 Section II - Setup Redshift Cluster with 1 node for intial usage.

Setup Redshift Cluster for First time.
1. Ensure default VPC is created
2. Create an IAM Role.


# Crawlers : 
This crawlers are responsible to create the metadata tables in Glue Catalog. These will crawl across the different datastores and make the metadata of the source data available on Glue DataCatalog. So, when ever we want to analyse the data present on S3 or any data store we can directly utilise the Athena and Glue Datacatalog Tables to view the data present on the Source Datastore like s3.

Crawler Partitions:
If we are having an s3 bucket and multiple folders in that which same schema/csv files. Its a good practice to partition them into different organized folders based on their categories. So that Glue can partition the folders data into single schema/table on the DataCatalog. This enables us to access all the files in the datastore with single metadata table on Datacatalog and just adjusting the queries to retrieve the data.

Athena can only be used to view the data present on S3 but not on Redshift.


