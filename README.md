# 🗓️ Vacation Tracking System (VTS)

## Vision
The aim of the **Vacation Tracking System (VTS)** is to provide employees with a self-service platform to manage their leave requests — whether annual, sick, or day-off — **without direct involvement from the HR department**.

---

## Domain
The system aims to **empower employees** to manage their own leave requests efficiently, which in turn **reduces the administrative workload** on the HR department and **minimizes manual processing** of employee leave records.

---

## Main Objectives
1. Decrease the workload on the Human Resources department.  
2. Empower employees to manage their own leave requests independently.

---

## Functional Requirements
1. The system must authenticate all users using **Single Sign-On (SSO)**.  
2. The system must authorize actions by roles — **Employee, HR, Admin, Manager** — users can only see actions allowed for their roles.  
3. Retrieve employee details from HR systems.  
4. Sync changes between the HR legacy system and the VTS.  
5. Display leave balances for each employee.  
6. Requests must be auto-approved based on preconfigured rules.  
7. Provide a request calendar — users can view requests **one year back** and **up to 1.5 years in the future**.  
8. Detect conflicts between requests.  
9. Allow employees to create new leave requests.  
10. Allow employees to view their request history.  
11. Provide configuration options for approval rules.  
12. Managers can approve or reject requests.  
13. Send email notifications for all request updates.  
14. HR and Admin users can override rules.  
15. Log all overrides.  
16. Managers can award personal leave within system limits.  
17. Log all transactions for auditing.  
18. Provide an API to query request details for integration with other internal systems.

---

## Constraints
1. The system will **not** be a standalone solution — it must be built as an **extension of the existing intranet portal**.  
2. Authentication must use the **SSO mechanism**.  
3. Only **HR clerks** and **Admins** can bypass validation rules.  
4. All overrides must be logged.  
5. Manager approval is optional, based on company policy.  
6. The request calendar (view range) is fixed by design.  
7. The system must run on **existing middleware and hardware**.  
8. Managers can only award personal leave **within configured limits**.  
9. All transactions must be logged.  
10. The system is restricted to the **internal company network** (intranet scope).

---

## Actors and Roles
### 1. Employees
- Submit leave requests (annual, sick, or personal).  
- View request history and balances.  

### 2. HR Clerk
- View employee details.  
- Ensure reliability and accuracy of employee data.  
- Add or remove employee records.  
- May have **two IDs** — one as a clerk, and one as an employee.  

### 3. Manager
- Approve or reject employee leave requests.  
- Award additional leave (within system-set limits).  

### 4. System Administrator
- Manage technical resources, configurations, and access controls.  


