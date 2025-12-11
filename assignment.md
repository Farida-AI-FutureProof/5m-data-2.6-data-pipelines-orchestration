# Assignment

## Brief

Write the commands for the following questions.

### Question 1

Question: Insert the command in the following steps to extract data from a PostgreSQL database and load it into a BigQuery dataset using Meltano.

Answer:

```bash
# Assignment 2.6 – Data Pipelines with Meltano

This assignment demonstrates how to extract data from PostgreSQL and load it into a BigQuery dataset using Meltano.

## Question 1

**Insert the Meltano command for each of the following steps.**

```bash
# Step 1: Add the tap-postgres extractor
meltano add extractor tap-postgres

# Step 2: Configure the extractor with the PostgreSQL connection details (interactive option)
meltano config tap-postgres set host <POSTGRES_HOST>
meltano config tap-postgres set port <POSTGRES_PORT>
meltano config tap-postgres set user <POSTGRES_USER>
meltano config tap-postgres set password <POSTGRES_PASSWORD>
meltano config tap-postgres set database <POSTGRES_DATABASE>

# Step 3: Add the target-bigquery loader
meltano add loader target-bigquery

# Step 4: Configure the BigQuery loader with project, dataset, and service account details
meltano config target-bigquery set project_id <BIGQUERY_PROJECT_ID>
meltano config target-bigquery set dataset <BIGQUERY_DATASET>
meltano config target-bigquery set credentials_path <PATH_TO_SERVICE_ACCOUNT_JSON>

# Step 5: Run the pipeline
meltano run tap-postgres target-bigquery



```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
