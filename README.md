 **System Requirements Specification & Process Automation Design for Informal Micro-Retail Operations**

---

##  Project Overview
Informal township retail enterprises (spaza shops) often rely on manual, paper-based tracking, leading to stock leakage, untracked cash usage, and inaccurate daily sales reconciliation. 

This repository presents a **Systems Analysis & Automation Feasibility Design** for **Semenya Tuckshop**, a family-owned micro-retail business in Mpumalanga, South Africa. It bridges traditional manual retail operations with modern system automation to streamline inventory management, point-of-sale (POS) rules, and financial reporting.

---

##  Key System & Business Logic Addressed

* **Automated Bulk-to-Unit Conversion:** System logic that automatically breaks down wholesale inventory (e.g., bulk box of spice sachets or cigarette bricks) into individual retail unit stock deductions upon purchase.
* **Perishable & Fast-Prep Recipe Deductions:** Automated Bill-of-Materials (BOM) stock tracking for prepared items (e.g., slap chips and kotas) based on individual ingredient usage.
* **Payment Surcharge & Card Rules:** Configurable transaction fee logic for electronic card payments vs. direct cash sales (e.g., FNB Speedpoint card surcharge handling).
* **End-of-Day (EOD) Automated Reconciliation:** Matching daily till cash, mid-day vendor payouts, and card transactions against recorded POS sales to identify variances.


## 🛠️ Repository Artifacts & Structure

```text
Spaza-Shop-Automation/
│
├── 01-requirements/
│   ├── business-requirements.md       <-- As-Is vs. To-Be, Problem Statement & Scope
│   ├── user-stories.md                <-- Agile Backlog with Given/When/Then Criteria
│   └── functional-specifications.md   <-- Bulk conversion, surcharge & BOM business rules
│
├── 02-process-maps/
│   ├── as-is-manual-sales-flow.png    <-- Baseline manual process (BPMN 2.0)
│   └── to-be-automated-pos-flow.png   <-- Automated system workflow (BPMN 2.0)
│
├── 03-system-design/
│   ├── use-case-diagram.png           <-- UML Use Case Diagram
│   ├── sequence-diagram.png           <-- Order processing & stock deduction sequence
│   └── domain-class-diagram.png       <-- ERD / Domain Model (Products, Batches, Sales)
│
└── 04-data-and-analytics/
    ├── schema.sql                     <-- Database tables & constraints
    └── analytical-queries.sql         <-- SQL for daily recon, variance & reorder alerts
