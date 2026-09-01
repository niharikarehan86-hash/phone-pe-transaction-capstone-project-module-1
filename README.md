# PhonePe Transaction Dispute Analyzer

## 📌 Project Overview

The **PhonePe Transaction Dispute Analyzer** is a Python-based transaction support and dispute-analysis tool developed in **Google Colab**.

The purpose of this project is to help support and operations teams identify problematic transactions, analyze refunds and customer complaints, track support tickets, determine dispute priority, and recommend appropriate actions.

The project combines information from multiple datasets and converts raw transaction and support data into meaningful, business-readable reports.

---

## 🎯 Project Objectives

The main objectives of this project are:

1. **Load and integrate multiple datasets** related to transactions, customers, merchants, refunds, complaints, support tickets, and status notes.

2. **Validate the datasets** by checking columns, missing values, duplicates, invalid records, and relationships between datasets.

3. **Clean and standardize data** so that inconsistent statuses, dates, amounts, payment modes, and other fields can be analyzed reliably.

4. **Analyze transaction health** by identifying successful, failed, pending, and reversed transactions.

5. **Analyze refund issues** including pending refunds, refund delays, SLA breaches, failed refunds, partial refunds, missing refund records, and amount mismatches.

6. **Analyze customer complaints** and identify complaint severity, repeated complaints, sentiment, and complaint-related issues.

7. **Analyze support tickets** including ticket status, severity, age, escalation, and SLA-related problems.

8. **Identify suspicious or duplicate transactions** where applicable.

9. **Classify dispute priority** using the required hierarchy:

   **P0 > P1 > P2 > P3 > No Issue**

10. **Generate recommended actions** based on the identified transaction and support issues.

11. **Generate final reports** that can be used by support and operations teams.

12. **Provide a simple Google Colab GUI** using `ipywidgets` for transaction searching and filtering.

---

## 🏗️ Project Workflow

```text
Raw Datasets
     ↓
Data Loading
     ↓
Data Validation
     ↓
Data Cleaning & Standardization
     ↓
Transaction Analysis
     ↓
Refund & SLA Analysis
     ↓
Complaint Analysis
     ↓
Support Ticket Analysis
     ↓
Duplicate / Suspicion Analysis
     ↓
Feature Integration
     ↓
Dispute Priority Classification
     ↓
Recommended Action
     ↓
Final Reports
     ↓
Colab Search & Filter GUI
```

---

## 📂 Datasets

The project works with multiple data sources, including:

* `transactions.csv`
* `refunds.xlsx`
* `customer_complaints.json`
* `support_tickets.csv`
* `customers.csv`
* `merchants.csv`
* `status_notes.txt`

These datasets are combined to create a complete view of a transaction dispute case.

---

## 🔍 Key Analysis Areas

### 1. Transaction Analysis

The system analyzes transaction status and identifies:

* Successful transactions
* Failed transactions
* Pending transactions
* Reversed transactions
* Transaction success/failure rates
* Failed transaction amounts

---

### 2. Refund Analysis

The refund module identifies different refund situations, such as:

* Refund completed on time
* Refund delay warning
* Refund SLA breach
* Refund failed
* Refund record missing
* Partial refund
* Refund amount mismatch

This helps the support team identify customers whose refund cases require attention.

---

### 3. Complaint Analysis

Customer complaints are linked with transactions to identify:

* Complaint count
* Customer complaint history
* Complaint status
* Complaint type
* Sentiment
* Complaint severity
* Repeated complaints

---

### 4. Support Ticket Analysis

Support tickets are analyzed using information such as:

* Ticket count
* Ticket status
* Assigned team
* Escalation status
* Ticket age
* Ticket severity
* Ticket issue/SLA tags

---

## 🚦 Dispute Priority

After analyzing all available information, each transaction is assigned a single dispute priority.

The priority hierarchy is:

```text
P0
 ↓
P1
 ↓
P2
 ↓
P3
 ↓
No Issue
```

A `priority_reason` is also generated to explain why a particular priority was assigned.

---

## 🖥️ Colab GUI

The project includes a simple interface using **`ipywidgets`**.

An operations user can:

* Search using a transaction ID
* View a transaction case summary
* Filter transactions by priority
* Filter by refund issue/status
* Filter by payment mode
* Filter by city
* Filter by ticket status
* Filter by merchant category
* Handle invalid transaction IDs with a friendly message

The GUI is designed to work directly inside Google Colab and does not require a separate web application.

---

## 🛠️ Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **ipywidgets**
* CSV file handling
* Excel file handling
* JSON file handling
* Data validation and cleaning

---

## 📊 Final Outputs

The completed project produces business-oriented reports containing information about:

* Transaction details
* Customer information
* Merchant information
* Refund status
* Complaint information
* Support tickets
* Detected issues
* Dispute priority
* Priority reason
* Recommended action

The notebook also provides previews of the final reports.

---

## 🐛 Debugging & Improvement

This project started from an incomplete codebase created by a previous developer.

The implementation therefore includes debugging and completion of areas such as:

* File loading
* Data validation
* Data cleaning
* Refund SLA calculations
* Complaint processing
* Ticket processing
* Priority classification
* Report exports
* Colab GUI

A debug-fix log is maintained to document important issues, their root causes, fixes, and testing status.

---

## 📋 Project Deliverable

The required final submission is:

**One completed Google Colab notebook.**

The notebook should contain:

* Working implementation
* Visible outputs
* Debug fix log
* AI prompt usage log
* PRD completion mapping
* Assumption and limitation log
* Final report previews
* Product walkthrough
* Evaluation-ready explanation

The notebook may generate CSV files as product outputs, but these are not separate required submissions.

---

## ▶️ How to Run

### Step 1: Open Google Colab

Open the completed `.ipynb` notebook in Google Colab.

### Step 2: Add the Required Datasets

Place the required input files in the expected project/data location.

### Step 3: Run the Notebook

Run the notebook cells sequentially from beginning to end.

### Step 4: Review Validation

Check the data-validation output and ensure the datasets have been loaded correctly.

### Step 5: Review Analysis

Review transaction, refund, complaint, ticket, priority, and recommended-action outputs.

### Step 6: Use the GUI

Use the transaction search and filter interface to investigate individual cases.

---

## 👥 Intended Users

The main users of this project are:

* Support executives
* Support operations teams
* Operations analysts
* Transaction-dispute teams

The tool helps them quickly understand transaction cases and focus on higher-priority problems.

---

## 🎯 Business Value

The project converts multiple raw data sources into a structured dispute-analysis system.

Instead of manually checking transaction, refund, complaint, and ticket records separately, an operations user can view the combined case information, identify the severity of the issue, determine its priority, and understand the recommended next action.

---

## ⚠️ Assumptions & Limitations

* The analysis depends on the quality and completeness of the input datasets.
* Business rules and priority classifications should follow the provided PRD.
* The GUI is designed specifically for Google Colab using `ipywidgets`.
* This project is an internal support-operations case study and is not intended to be a production payment-processing system.

---

## 📌 Summary

**PhonePe Transaction Dispute Analyzer** is a Python and Google Colab-based support analytics project that:

**Loads → Validates → Cleans → Analyzes → Integrates → Prioritizes → Recommends → Reports**

Its primary goal is to help support teams identify transaction disputes and determine which cases require attention and what action should be taken.
