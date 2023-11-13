# IDS Mini Project 11

This repository contains a series of Databricks notebooks designed to construct a data processing pipeline for musical track analysis. The pipeline is built using PySpark and SQL within the Databricks environment, leveraging the powerful distributed computing capabilities of Apache Spark. 

The initial script sets up a structured streaming job to ingest data continuously from a specified file path, using the `cloudFiles` format for robust and efficient file processing. The data schema is explicitly defined to match the input CSV files, ensuring proper column data types and handling of nullable fields. Once ingested, the data is streamed into the `raw_song_data` table, with checkpoints enabled for fault tolerance and to manage streaming state.

Subsequent SQL scripts in the notebooks focus on data transformation and analysis. The `prepared_song_data` table is created to hold a more refined view of the raw song data, including a timestamp to track processing time. Data is inserted into this table after being selected and formatted from `raw_song_data`. Analytical queries are then executed against `prepared_song_data` to derive insights such as the artists with the most song releases per year and song recommendations for a DJ list based on time signature and tempo criteria. 

These Databricks notebooks exemplify how to seamlessly combine structured streaming with batch processing for data analysis tasks, all within the unified analytics platform provided by Databricks.
![Alt text](<Screen Shot 2023-11-12 at 7.32.58 PM.png>)