 🏦 Airflow Transaction Data Pipeline

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

<img width="946" height="424" alt="Screenshot 2026-04-09 125502" src="https://github.com/user-attachments/assets/601bd745-4819-413a-9757-028574e1c1d2" />
<img width="947" height="392" alt="Screenshot 2026-04-09 125352" src="https://github.com/user-attachments/assets/82f83c68-bbca-4595-bd6b-065e61f5f658" />

