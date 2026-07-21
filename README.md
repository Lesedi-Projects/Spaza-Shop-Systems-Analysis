# Micro-Retail Systems Analysis — Semenya Tuckshop, Mpumalanga

## Overview
A systems analysis and automation design study for a real micro-retail enterprise — Semenya Tuckshop, located in Tweefontein K, Sesakhile, Mpumalanga — conducted as part of a BCom Honours in Management Information Systems at the University of Cape Town (2026).

The study applies formal systems analysis methodologies to a real informal economy business, demonstrating how structured BA and systems analysis techniques can be applied to small enterprises that are typically excluded from enterprise technology conversations.

---

## Why This Matters
South Africa's informal retail sector — spaza shops, tuck shops, and micro-traders — represents a significant portion of economic activity in township and rural communities. These businesses operate largely without formal systems, making them vulnerable to stock loss, revenue leakage, and operational inefficiency.

This project asks: what would it look like to apply professional systems analysis to a business like Semenya Tuckshop — and what automation opportunities exist within existing constraints like limited connectivity, cash-dominant transactions, and low technology literacy?

---

## Business Context
- **Business name:** Semenya Tuckshop
- **Location:** Tweefontein K, Sesakhile, Mpumalanga
- **Business type:** Micro-retail / informal tuck shop
- **Operating since:** Prior to 2011
- **Current technology:** Cash register, FNB Speedpoint card machine
- **Current inventory management:** Manual stock taking
- **Stock model:** Bulk purchasing, unit-level selling

---

## Methodology
This project applies the following frameworks and techniques studied in the UCT Honours BASA programme:

- **Systems Development Life Cycle (SDLC)** — structured analysis from current state through to system design
- **Agile methodology** — iterative, user-centred approach to requirements and solution design
- **Use Case Analysis** — identifying actors, use cases, and system interactions
- **Use Case Narratives** — detailed description of how each system interaction unfolds
- **User Stories** — Agile format requirements capturing what each actor needs the system to do
- **Data Modelling** — entity identification and relationship mapping for a proposed system
- **Process Mapping** — AS-IS manual operations documented and TO-BE automated workflows designed

---

## Project Deliverables

### 1. AS-IS Analysis
Documents the current manual operations of Semenya Tuckshop across four key business functions:
- Stock receiving and bulk-to-unit conversion
- Inventory tracking and stock taking
- Point of sale and payment processing
- Daily sales recording and cash reconciliation

### 2. Use Case Diagram
Visual representation of the proposed system's actors and use cases — showing who interacts with the system and what they need it to do.

**Actors identified:**
- Shop Owner / Operator
- Customer
- Supplier
- System (automated processes)

**Key use cases:**
- Record stock received
- Convert bulk to unit quantities
- Process sale transaction
- Generate daily sales report
- Trigger low stock alert
- Reconcile cash against system sales

### 3. Use Case Narratives
Detailed step-by-step descriptions of how each use case unfolds — including main success scenarios, alternative flows, and exception handling.

### 4. User Stories (Agile Format)
Requirements expressed in Agile user story format:

*"As a shop owner, I want to record stock received in bulk so that I can track how many units are available for sale."*

*"As a shop owner, I want the system to alert me when stock falls below a minimum threshold so that I can reorder before running out."*

*"As a shop owner, I want to generate a daily sales summary so that I can reconcile my cash drawer at end of day."*

*"As a customer, I want to pay using my bank card so that I do not need to carry cash."*

*"As a shop owner, I want to see which products sell fastest so that I can make better bulk purchasing decisions."*

### 5. Data Model
Entity-relationship model identifying the core data entities and their relationships for the proposed system:

**Key entities:**
- **Product** (`ProductID`, `Name`, `Category`, `UnitPrice`, `BulkUnit`, `UnitsPerBulk`)
- **Stock** (`StockID`, `ProductID`, `QuantityInStock`, `ReorderLevel`, `LastUpdated`)
- **Sale** (`SaleID`, `DateTimeStamp`, `TotalAmount`, `PaymentMethod`)
- **SaleLineItem** (`LineItemID`, `SaleID`, `ProductID`, `Quantity`, `UnitPrice`)
- **Supplier** (`SupplierID`, `Name`, `ContactNumber`, `ProductsSupplied`)
- **StockReceipt** (`ReceiptID`, `SupplierID`, `DateReceived`, `ProductID`, `BulkQuantity`)

### 6. Automation Opportunities Identified
Based on the AS-IS analysis, the following automation opportunities were identified:

| Manual Process | Automation Opportunity | Feasibility |
|---|---|---|
| Manual stock counting | Automated stock deduction per sale | High — integrates with POS |
| Bulk-to-unit conversion calculated mentally | System rule: Units = BulkQty × UnitsPerBulk | High — simple logic |
| No low stock alerts | Automated alert when stock < reorder level | High — rule-based |
| Manual cash reconciliation | System-generated daily sales report vs cash | High — automated |
| No sales trend visibility | Weekly sales summary by product | Medium — requires data history |
| Paper-based supplier orders | Digital reorder trigger to supplier | Low — requires supplier adoption |

### 7. Recommended System Approach
Given the operational constraints — limited connectivity, cash-dominant transactions, low technology literacy, and cost sensitivity — the recommended approach is:

- **Agile delivery** — start with the highest-value, lowest-complexity features first
- **Mobile-first design** — accessible on a basic Android smartphone without constant internet connectivity
- **Offline-first architecture** — data captured offline and synced when connectivity is available
- **Sprint 1 priority:** Stock management and bulk-to-unit conversion logic
- **Sprint 2 priority:** POS transaction recording and daily sales report
- **Sprint 3 priority:** Low stock alerts and supplier reorder triggers

---

## Connection to Career Focus
This project demonstrates that systems analysis and automation design are not limited to large enterprises. The same methodologies — use cases, user stories, data modelling, process redesign — apply equally to a tuck shop in Mpumalanga and a multinational corporation.

The informal economy serves millions of South Africans who depend on these businesses daily. Technology designed with and for these businesses — not just for enterprise clients — is where genuine social impact lives.

---

## Frameworks Applied
| Framework | Application |
|---|---|
| SDLC | Structured analysis from AS-IS through system design |
| Agile / SCRUM | Sprint-based delivery planning and user stories |
| Use Case Analysis | Actor and interaction identification |
| Entity-Relationship Modelling | Data structure design |
| Process Mapping | AS-IS manual workflow documentation |
| Automation Assessment | Feasibility scoring of automation opportunities |

---

## Status
- [x] AS-IS business context documented
- [x] Use case diagram drafted
- [x] Use case narratives written
- [x] User stories defined
- [x] Data model designed
- [x] Automation opportunities identified
- [ ] TO-BE system wireframes (planned)
- [ ] Prototype (future scope)

---

## Author
**Lesedi Mahlangu**  
BCom Accounting — University of the Witwatersrand (2024)  
BCom Honours in Management Information Systems — UCT (2026)  
📧 mahlangulesedi34@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/lesedi-mahlangu-13702b22b/)  
🌐 [Portfolio](https://lesedimahlangu.carrd.co/)
