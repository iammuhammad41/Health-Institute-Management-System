# Health Institute Management System  
**Oracle Forms 10g & Oracle Database 10g**

A centralized, modular HIS for clinics and small hospitals—managing patients, appointments, billing, pharmacy, labs, staff and reporting via Oracle Forms/Reports on a 10g database.



## 📖 Project Overview

This Health Institute Management System provides:

- **Secure Login & Role‑Based Access**  
- **Patient Registration & Demographics**  
- **Appointment Scheduling & Clinic Workflow**  
- **Doctor & Staff Management**  
- **Outpatient & Inpatient Billing**  
- **Pharmacy Dispensing & Inventory**  
- **Laboratory Test Entry & Results**  
- **Medical Records & Notes**  
- **Reports & Dashboards**  

Built with Oracle Forms 10g/Reports and backed by Oracle 10g Database.


## 📂 Repository Contents

- `login_test.fmb` / `login_test.fmx`  
  – Login & authentication form

> _Other `.fmb`/`.fmx` modules can be added here for each feature._



## 🏗️ Main Modules & Forms

| Module                          | Forms Source (`.fmb`)           | Forms Executable (`.fmx`)          | Description                                             |
|:--------------------------------|:--------------------------------|:-----------------------------------|:--------------------------------------------------------|
| **Login & Security**            | `login_test.fmb`                | `login_test.fmx`                   | User authentication & role management                   |
| **Patient Registration**        | `patient_reg.fmb`               | `patient_reg.fmx`                  | Demographics, insurance, contact info                    |
| **Appointment Scheduling**      | `appointments.fmb`              | `appointments.fmx`                 | Book, reschedule, cancel patient visits                 |
| **Doctor & Staff Management**   | `staff_mgmt.fmb`                | `staff_mgmt.fmx`                   | Doctor profiles, departments, staff scheduling           |
| **Billing & Accounts**          | `billing.fmb`                   | `billing.fmx`                      | Generate invoices, process payments, insurance claims    |
| **Pharmacy & Inventory**        | `pharmacy.fmb`                  | `pharmacy.fmx`                     | Dispense drugs, track stock levels, reorder alerts       |
| **Laboratory Management**       | `lab_tests.fmb`                 | `lab_tests.fmx`                    | Enter test orders & results for hematology, biochemistry|
| **Medical Records**             | `med_records.fmb`               | `med_records.fmx`                  | View & update patient history, clinical notes            |
| **Reports & Analytics**         | `reports_menu.fmb`              | `reports_menu.fmx`                 | Operational, financial, compliance reports               |


## 🛠️ Prerequisites

1. **Oracle Database 10g**  
2. **Oracle Forms 10g Developer & Runtime**  
3. **Oracle Reports 10g** (for `.rdf` or `.rep` report modules)  
4. **PL/SQL** for triggers & stored procedures  
5. **Forms Server** configured with Forms Services  


## 🚀 Installation & Deployment

1. **Database Schema**  
   - Run `schema.sql` to create tables:  
     `USERS`, `PATIENTS`, `APPOINTMENTS`, `STAFF`, `BILLS`, `PHARMACY_STOCK`, `LAB_RESULTS`, etc.  
   - Grant necessary privileges to the Forms schema user.

2. **Compile Forms**  
   - Open each `.fmb` in Oracle Forms Developer → **Compile → Generate Form Module** → produce `.fmx`.  
   - Deploy all `.fmx` files to your Forms Server directory.

3. **Configure Forms Services**  
   - Add entries in `formsweb.cfg` for each form.  
   - Ensure `FORMS_PATH` includes your deployment directory.

4. **Compile & Register Reports**  
   - Compile `.rdf`/`.rep` modules and register them on the Reports Server.

5. **Launch Application**  
   - Access via browser/Java Applet, e.g.:  
     ```
     http://<forms-server>:<port>/forms/frmservlet?config=default&form=login_test.fmx
     ```
