# Big-Data-Pipeline-with-Pyspark
In this project, I built a Batch End-to-end Big data pipeline using Hadoop, Hive, and Pyspark with USA Prescriber Dataset.

## Tech that is used in this project
1. Python 3
2. Java Development Kit (JDK) 8
3. Google Cloud Platform (Virtual Machine)
4. Hadoop HDFS and YARN ver. 3.3.4
5. PostgreSQL in Docker Container
6. Hive ver 3.1.2
7. Apache Spark ver 3.2.1
8. Amazon S3 Bucket

## Data Set
The data set that was used in this project are:
1. USA_prexc_Medicare_Data_2021.csv
2. us_cities_dimension.parquet

## Goal of this Project
The goal of this project is to build an end-to-end data pipeline from ingestion data, preprocessing data, transforming data, and extracting data to PostgreSQL and HIVE, and copy the data to Amazon S3 Bucket

## Project Approach
While building this Project I used Pycharm in Windows for Testing and Debugging the Code, and then deployed the code at a single-node cluster on the Google Cloud Platform

## Code
I built the code as a module on a separate Python file,  integrated all the code on the main Python file, and added validation, Logging, and Error handling for better use
All of the Python code for this project are :
1. run_presc_pipeline.py as main Python code
2. get_all_variables.py for storing all variables that were used in this project
3. create_objects.py for building spark object
4. presc_run_data_ingest.py for starting the ingestion process
5. presc_run_data_pre_processing.py for starting the preprocessing process
6. presc_run_data_transform.py for starting the transforming process
7. presc_run_data_extraction.py for starting the extraction process
8. presc_run_data_persist.py for persisting data to PostgreSQL and HIVE
9. validations.py for the validation process

Aside from the Python file, there is logging_to_file.conf for handling Logging with Custom Logger and The Korn Shell (ksh) script for automating processes in a Single Node Cluster. All of the ksh scripts are:
1. copy_files_local_to_hdfs.ksh to copy the input file to Hadoop HDFS
2. copy_files_hdfs_to_local.ksh to get the transformed data from Hadoop HDFS to Local
3. copy_files_to_s3.ksh to copy the transformed data to S3 Bucket
4. run_prescPipeline_project.ksh to integrate all of the Python and ksh scripts so all of the processes can be run with a single script
