# EMR Data Standardization Pipeline with Airflow

## Project Summary
Automated the ingestion and normalization of multimodal Electronic Medical Records (EMR) from three hospitals using Apache Airflow. Reduced data preparation time by 70% and improved downstream ML pipeline efficiency.

## Problem Statement
Each hospital maintained its own EMR format, schema, and data conventions, making unified analytics and modeling nearly impossible. A standardized data pipeline was needed to transform disparate inputs into a consistent format.

## Tools & Technologies Used
- **Languages**: Python, SQL  
- **Workflow Orchestration**: Apache Airflow  
- **Data Sources**: EMR data (structured/unstructured), HL7 messages, lab records  
- **Storage**: AWS S3, PostgreSQL, internal hospital systems

## Pipeline Features
- Ingested HL7, CSV, and JSON files from hospital endpoints  
- Applied hospital-specific normalization logic using Python operators  
- Consolidated data into a unified relational schema in PostgreSQL  
- Handled data dependencies with Airflow DAGs and dynamic task mapping

## Architecture Overview
```
Hospital A/B/C ─▶ S3 Intake ─▶ Airflow DAG ─▶ Transformation Scripts ─▶ Unified PostgreSQL DB ─▶ Downstream ML / Dashboards
```

## Results & Business Impact
- **70% reduction in manual preparation time**  
- Enabled real-time access to patient history across sites  
- Supported diagnostics, patient monitoring, and predictive analytics workflows

## Monitoring & Maintenance
- SLA monitoring and retry logic implemented in Airflow  
- Error logs sent to centralized monitoring dashboard for auditing

## Challenges & Learnings
- Handled schema drift by versioning transformation logic  
- Built reusable task templates to minimize code duplication  
- Ensured HIPAA compliance through anonymization and access control

## Team Collaboration
- Worked directly with hospital IT departments and clinicians  
- Provided data documentation and pipeline visibility via Airflow UI

## Code Availability
Due to healthcare data confidentiality, pipeline scripts and hospital datasets are not publicly available.
