# DE-Zoomcamp-2026-Homework-2-WorkflowOrchestration-Kestra

This Readme provides the solutionto the Week 2 module homework
## Assignment
Your task is to extend the existing flows to include data for the year 2021 (data exists i.e. from 2021-01-01 to 2021-07-31).
After setting up the GCP account and running the [Docker Compose YAML](docker-compose.yml), the Kestra flows for [GCP setup](Kestra_flow_gcp_setup) and retrieving the [key–value pairs](Kestra_flow_get_kv) were executed.

To upload the Green and Yellow taxi datasets into BigQuery, an [ELT flow](ELT_NYCTaxi_Gcp) was created. By setting the time period for backfill executions from **2021-01-01 00:00:00** to **2021-07-02 00:00:00**, the data for the year 2021 was loaded into BigQuery.


## Quiz Questions
Complete the quiz shown below. It's a set of 6 multiple-choice questions to test your understanding of workflow orchestration, Kestra, and ETL pipelines.

### Within the execution for Yellow Taxi data for the year 2020 and month 12: what is the uncompressed file size (i.e. the output file yellow_tripdata_2020-12.csv of the extract task)?
Using [File size flow ](Kestra_flow_file_size)
 - 128.3 MiB 

### What is the rendered value of the variable file when the inputs taxi is set to green, year is set to 2020, and month is set to 04 during execution?

- green_tripdata_2020-04.csv

### How many rows are there for the Yellow Taxi data for all CSV files in the year 2020?
Using [count rows flow](Kestra_flow_count_rows)
- 24,648,499

### How many rows are there for the Green Taxi data for all CSV files in the year 2020?
Using [count rows flow](Kestra_flow_count_rows)
- 1,734,051

### How many rows are there for the Yellow Taxi data for the March 2021 CSV file?
From uploaded tables in BigQuery
- 1,925,152

### How would you configure the timezone to New York in a Schedule trigger?

- Add a timezone property set to America/New_York in the Schedule trigger configuration

