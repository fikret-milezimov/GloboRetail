# GloboRetail Data Pipeline

## Description

GloboRetail is a configuration-driven ETL pipeline built with Apache Airflow.
The project processes retail sales data through several stages including extraction, validation, transformation, and loading into analytics-ready datasets.

The goal of the project is to demonstrate a modular and scalable data pipeline architecture that can automate data processing workflows.

---

## Deployment

This project runs in a local Apache Airflow environment.

The pipeline can be executed through Airflow DAGs using the Astro CLI.

Example:

```bash
astro dev start
```

Once the Airflow environment is running, the pipeline can be triggered from the Airflow web interface.

---

## Technology Stack

* Python
* Apache Airflow
* Pandas
* YAML configuration
* Pandera (data validation)
* Snowflake / Data Warehouse concepts
* Git

---

## Pipeline Architecture

The ETL pipeline follows a layered data architecture:

```
Raw Data
   │
   ▼
Extract Layer
   │
   ▼
Validation Layer
   │
   ▼
Transformation Layer
   │
   ▼
Analytics / Reporting Tables
```

Each step of the pipeline is executed as a task within an Airflow DAG.

---

## Pipeline Flow

The main pipeline consists of the following stages:

1. **Extract**
   Raw retail data is collected from source files.

2. **Validation**
   Data schemas are validated using Pandera to ensure correct structure and data quality.

3. **Transformation**
   Data is cleaned and transformed into analytics-ready formats.

4. **Load**
   The processed data is stored in structured tables ready for analysis and reporting.

---

## Project Structure

```
GloboRetail
│
├── dags/
│   └── retail_pipeline.py
│
├── pipelines/
│   ├── extract.py
│   ├── validate.py
│   ├── transform.py
│   └── load.py
│
├── schemas/
│   └── validation_schema.py
│
├── config/
│   └── pipeline_config.yaml
│
└── README.md
```

This modular structure keeps the pipeline easy to extend and maintain.

---

## Screenshots

### Airflow DAG

![Airflow DAG](Screenshots/dag.png)

### Pipeline Execution

![Pipeline Run](Screenshots/pipeline_run.png)

---

## Future Improvements

Possible future improvements include:

* Integration with cloud storage (AWS S3)
* Automated monitoring and alerting
* Additional data validation rules
* Deployment in a production environment

---

## Author

Fikret Milezimov

GitHub: https://github.com/fikret-milezimov
