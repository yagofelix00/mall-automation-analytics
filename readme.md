# Mall Automation Analytics

Automated data pipeline designed to generate daily store performance reports, organize sales data by shopping mall, and send personalized email dashboards to store managers and the board of directors.  
This project centralizes sales information, creates individual Excel files per store, evaluates KPI results against predefined goals, and delivers OnePage-style performance summaries automatically via Outlook.

---

## 📌 Overview

The **Mall Automation Analytics** system processes daily sales data from multiple stores and automates the entire workflow of:

- Importing and cleaning raw data  
- Merging store information  
- Splitting sales into independent datasets per store  
- Creating daily backup folders for each shopping mall  
- Generating Excel reports dynamically  
- Calculating daily and yearly KPIs  
- Formatting status indicators (green/red)  
- Sending personalized performance emails to managers  
- Sending daily rankings to the board of directors  

This automation eliminates manual reporting work and ensures that all stakeholders receive updated KPIs every day.

---

## 🚀 Features

### **1. Data Integration**
- Reads data from:
  - `Emails.xlsx`  
  - `Lojas.csv`  
  - `Vendas.xlsx`  
- Merges sales with store metadata automatically.

### **2. Store-Level Data Separation**
Automatically creates a dictionary where each key represents a store, containing only its filtered sales.

### **3. Backup Folder Automation**
For each store:
- Creates a folder under `Backup Arquivos Lojas/`
- Generates an Excel file named:


### **4. KPI Calculation**
KPIs calculated daily and yearly:

- **Revenue**
- **Product diversity**
- **Average ticket size**

KPI goals are compared against each store result, generating green/red indicators.

### **5. Automated Email Notifications**
Using **Outlook + win32com**, the system sends:

#### ✔ Email to each manager with:
- OnePage HTML report  
- KPI indicators  
- Attached Excel file with the daily data  

#### ✔ Email to the board with:
- Best and worst stores of the day  
- Best and worst stores of the year  
- Ranking spreadsheets attached  

### **6. Fully Automated Workflow**
Running the script once completes the entire process without manual intervention.

---

## 📂 Project Structure

mall-automation-analytics/
│
├── Bases de Dados/
│ ├── Emails.xlsx
│ ├── Lojas.csv
│ └── Vendas.xlsx
│
├── Backup Arquivos Lojas/
│ ├── Store A/
│ │ └── {date}_StoreA.xlsx
│ └── Store B/
│ └── {date}_StoreB.xlsx
│
├── Automacao de Processo/
│ └── main.py (script principal)
│
└── README.md