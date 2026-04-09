<img width="959" height="491" alt="Screenshot 2026-04-09 125547" src="https://github.com/user-attachments/assets/706f43bb-65a5-4d3c-9b8f-a72b69108c44" /><img width="959" height="491" alt="Screenshot 2026-04-09 125547" src="https://github.com/user-attachments/assets/706f43bb-65a5-4d3c-9b8f-a72b69108c44" /># 🏦 Airflow Transaction Data Pipeline

## 📝 Project Description
This project implements a robust **Data Engineering pipeline** using **Apache Airflow** to automate the processing of financial transactions. The DAG orchestrates a flow starting from data ingestion, processing, and finally sending an automated report via email.

Key features:
- Modular design using Python scripts
- Automated scheduling every 10 minutes
- Email notifications with transaction reports

## 🛠️ Tech Stack
- **Orchestration:** Apache Airflow
- **Language:** Python 3.x
- **Operators:** PythonOperator, BashOperator, EmailOperator
- **Communication:** SMTP Email Server

## 🔄 DAG Workflow (`transaction_pipeline`)
The pipeline consists of 5 main tasks:

1. **`task1_start`** (`PythonOperator`): Initializes the workflow.
2. **`task2_process_transactions`** (`PythonOperator`): Processes raw transaction data.
3. **`task3_run_script`** (`BashOperator`): Executes an external Python script (`/data/process_transactions.py`) to ensure modularity.
4. **`task4_read_report`** (`PythonOperator`): Reads the generated transaction report.
5. **`task5_send_email`** (`EmailOperator`): Sends the final `Transaction Report` to the administrator's email.

## 📁 File Structure
