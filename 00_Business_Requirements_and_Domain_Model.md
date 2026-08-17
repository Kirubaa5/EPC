# 00 — Business Requirements and Domain Model

**Project:** EPC ERP System  
**Domain:** Engineering, Procurement & Construction (EPC)  
**Platform:** ERPNext + Frappe Framework  
**Document Type:** Business Requirements & Domain Model  
**Version:** 1.0  
**Status:** Draft  

---

# 1. Purpose

This document defines the business foundation of the EPC ERP System before development begins.

It describes:

- EPC domain fundamentals
- Business objectives
- Business problems
- Project lifecycle
- Major EPC domains
- Business actors
- Core business entities
- High-level relationships
- Major business processes
- Business rules
- Data categories
- Domain boundaries
- Assumptions
- Constraints
- Open questions

This document focuses on **what the business needs**, not how the software will technically implement it.

Detailed ERPNext mapping, Frappe DocTypes, database design, workflows, APIs, UI, permissions, and technical architecture will be defined in later documents.

---

# 2. Project Vision

The goal is to build an integrated ERP system for the EPC domain using **ERPNext and the Frappe Framework**.

The system will connect major EPC business functions into a common platform.

The primary vision is:

```text
                    EPC ERP SYSTEM
                          │
          ┌───────────────┼───────────────┐
          │               │               │
          ▼               ▼               ▼
     ENGINEERING      PROCUREMENT     CONSTRUCTION
          │               │               │
          └───────────────┼───────────────┘
                          │
              ┌───────────┼───────────┐
              ▼           ▼           ▼
           QUALITY       HSE       PROJECT CONTROLS
              │           │           │
              └───────────┼───────────┘
                          ▼
                    COMMISSIONING
                          │
                          ▼
                       HANDOVER
```

The system should provide a common source of truth for project information, business transactions, documents, approvals, progress, costs, risks, and operational activities.

---

# 3. What Is EPC?

EPC stands for:

- **Engineering**
- **Procurement**
- **Construction**

EPC is a project delivery model commonly used for large engineering, industrial, energy, infrastructure, and construction projects.

In a typical EPC project, an organization is responsible for delivering a defined project scope according to contractual, technical, commercial, quality, schedule, and safety requirements.

A simplified lifecycle is:

```text
Client Requirement
        ↓
Project / Contract
        ↓
Planning
        ↓
Engineering
        ↓
Procurement
        ↓
Construction
        ↓
Inspection & Testing
        ↓
Commissioning
        ↓
Handover
        ↓
Project Closure
```

The phases do not necessarily occur strictly one after another.

In real EPC projects, multiple phases can overlap.

For example:

```text
Engineering ────────────────────────►
        Procurement ─────────────────────►
                Construction ───────────────►
                         Commissioning ─────────►
```

---

# 4. Business Context

EPC projects involve many departments, organizations, documents, transactions, approvals, and physical activities.

A single project may involve:

- Client
- EPC contractor
- Engineering teams
- Procurement teams
- Vendors
- Suppliers
- Subcontractors
- Construction teams
- Quality teams
- HSE teams
- Planning teams
- Cost control teams
- Document controllers
- Finance teams
- Commissioning teams
- Management

Each department produces and consumes information.

For example:

```text
Engineering
     ↓
Material Requirements
     ↓
Procurement
     ↓
Vendor
     ↓
Material Delivery
     ↓
Construction
     ↓
Quality Inspection
     ↓
Commissioning
     ↓
Handover
```

Therefore, the EPC ERP system must connect these processes instead of treating them as isolated systems.

---

# 5. Business Problems

## 5.1 Information Fragmentation

Project information may be distributed across:

- Excel files
- Emails
- Shared folders
- PDFs
- Paper records
- Separate software
- Manual registers
- Department-specific systems

This makes it difficult to maintain a single source of truth.

---

## 5.2 Poor Project Visibility

Management may not have immediate visibility into:

- Project progress
- Engineering progress
- Procurement status
- Material availability
- Construction progress
- Quality issues
- HSE issues
- Project costs
- Schedule performance
- Risks

---

## 5.3 Manual Processes

Manual data entry can cause:

- Human errors
- Duplicate records
- Delayed updates
- Inconsistent information
- Increased administrative work

---

## 5.4 Approval Delays

Many EPC processes require multiple approvals.

Examples:

```text
Purchase Requisition
        ↓
Department Approval
        ↓
Procurement Approval
        ↓
Management Approval
```

Without a structured workflow, approvals can become difficult to track.

---

## 5.5 Procurement Tracking Problems

A procurement transaction may involve many stages:

```text
Requirement
    ↓
Purchase Requisition
    ↓
RFQ
    ↓
Vendor Quotation
    ↓
Technical Evaluation
    ↓
Commercial Evaluation
    ↓
Approval
    ↓
Purchase Order
    ↓
Manufacturing
    ↓
Inspection
    ↓
Shipment
    ↓
Delivery
    ↓
Receipt
```

The system should provide traceability across this lifecycle.

---

## 5.6 Engineering Document Problems

EPC projects generate large numbers of engineering documents.

Examples:

- Drawings
- Specifications
- Datasheets
- Calculations
- Reports
- Technical documents

Without document control, users may accidentally use outdated revisions.

---

## 5.7 Cost Visibility Problems

Management needs visibility into:

- Budget
- Planned cost
- Committed cost
- Actual cost
- Forecast cost
- Variance

---

## 5.8 Schedule Problems

Delays in one business area can affect another.

For example:

```text
Engineering Delay
       ↓
Procurement Delay
       ↓
Material Delivery Delay
       ↓
Construction Delay
       ↓
Project Completion Delay
```

The system should allow these dependencies to be monitored.

---

# 6. Business Objectives

The EPC ERP system should achieve the following objectives.

## 6.1 Centralize Information

Create a centralized platform for project and business information.

## 6.2 Integrate Departments

Connect Engineering, Procurement, Construction, Quality, HSE, Planning, Cost, and other functions.

## 6.3 Improve Visibility

Provide real-time or near-real-time visibility into project execution.

## 6.4 Improve Traceability

Allow users to trace transactions from their origin to completion.

## 6.5 Reduce Manual Work

Automate repetitive processes where appropriate.

## 6.6 Improve Data Quality

Reduce duplicate and inconsistent data.

## 6.7 Improve Approval Management

Provide structured workflows and approval processes.

## 6.8 Improve Project Control

Monitor:

- Scope
- Schedule
- Cost
- Quality
- HSE
- Risk
- Progress

## 6.9 Improve Decision Making

Provide:

- Reports
- Dashboards
- KPIs
- Analytics

## 6.10 Create an Automation Foundation

The platform should support future:

- Workflow automation
- Notifications
- Scheduled jobs
- Business rules
- Analytics
- AI-assisted capabilities

---

# 7. Project Scope

## 7.1 Initial Scope

The initial EPC ERP domain includes:

1. Project Management
2. Contract Management
3. Engineering Management
4. Procurement Management
5. Vendor Management
6. Material Management
7. Construction Management
8. Quality Management
9. HSE Management
10. Planning and Scheduling
11. Cost Management
12. Document Control
13. Inspection and Testing
14. Risk Management
15. Change Management
16. Commissioning
17. Project Handover
18. Reporting
19. Dashboards
20. Workflow and Approval Management
21. User and Role Management
22. Audit and Traceability

---

# 8. EPC Project Lifecycle

## 8.1 High-Level Lifecycle

```text
Client Requirement
        ↓
Project Initiation
        ↓
Contract
        ↓
Project Planning
        ↓
Engineering
        ↓
Procurement
        ↓
Construction
        ↓
Inspection & Testing
        ↓
Commissioning
        ↓
Handover
        ↓
Project Closure
```

---

## 8.2 Project Initiation

A project may begin from:

- Client requirement
- Contract award
- Purchase order
- Business opportunity
- Internal project initiation

Initial information may include:

- Project name
- Project identifier
- Client
- Location
- Project type
- Contract
- Scope
- Estimated value
- Planned start date
- Planned completion date
- Project manager

---

## 8.3 Project Planning

The organization establishes:

- Project scope
- Work breakdown
- Schedule
- Budget
- Resources
- Procurement strategy
- Engineering plan
- Construction plan
- Quality plan
- HSE plan
- Risk plan

---

## 8.4 Engineering

Engineering defines the technical requirements required to execute the project.

Engineering may produce:

- Drawings
- Specifications
- Calculations
- Datasheets
- Technical reports
- Material requirements
- Equipment requirements
- Engineering deliverables

---

## 8.5 Procurement

Procurement converts approved requirements into purchased goods and services.

```text
Requirement
      ↓
Purchase Requisition
      ↓
RFQ
      ↓
Vendor Quotations
      ↓
Technical Evaluation
      ↓
Commercial Evaluation
      ↓
Approval
      ↓
Purchase Order
      ↓
Vendor Execution
      ↓
Inspection
      ↓
Shipment
      ↓
Delivery
      ↓
Receipt
```

---

## 8.6 Construction

Construction converts engineering information and procured resources into physical project work.

Typical activities include:

- Site preparation
- Civil works
- Structural works
- Mechanical installation
- Electrical installation
- Piping
- Instrumentation
- Equipment installation
- Testing
- Punch-list completion

---

## 8.7 Quality Management

Quality verifies that materials, engineering outputs, and construction activities satisfy defined requirements.

Examples:

- Inspections
- Tests
- Quality plans
- Inspection requests
- Test records
- NCRs
- Corrective actions
- Quality approvals

---

## 8.8 HSE Management

HSE manages:

- Health
- Safety
- Environmental requirements

Examples:

- Safety inspections
- Incidents
- Near misses
- Safety observations
- Permits
- Corrective actions
- Environmental observations

---

## 8.9 Commissioning

Commissioning verifies that completed systems and equipment are ready for operation.

Activities may include:

- Pre-commissioning
- Functional testing
- System testing
- Equipment testing
- Performance verification
- Punch-list closure

---

## 8.10 Handover

The project is handed over to the client after the required completion, testing, documentation, and contractual requirements are satisfied.

Handover may include:

- As-built documents
- Test records
- Inspection records
- Certificates
- Completion records
- Punch-list closure
- Acceptance records
- Operation and maintenance information

---

# 9. Major EPC Business Domains

## 9.1 Project Management

Responsible for overall project execution.

Key areas:

- Scope
- Schedule
- Cost
- Resources
- Risk
- Quality
- Communication
- Stakeholder management
- Reporting

---

## 9.2 Engineering

Responsible for technical design and engineering deliverables.

Possible disciplines:

- Civil
- Structural
- Mechanical
- Electrical
- Instrumentation
- Process
- Piping
- Architecture
- Specialized engineering

---

## 9.3 Procurement

Responsible for acquiring:

- Materials
- Equipment
- Services
- Subcontracted work

Key processes:

- Purchase requisitions
- RFQs
- Quotations
- Technical evaluations
- Commercial evaluations
- Purchase orders
- Expediting
- Inspection
- Delivery

---

## 9.4 Vendor Management

Responsible for:

- Vendor registration
- Vendor qualification
- Vendor evaluation
- Vendor performance
- Vendor documentation

---

## 9.5 Material Management

Responsible for:

- Material master
- Material categories
- Units of measure
- Material requirements
- Stock
- Delivery
- Receipt
- Inspection
- Allocation

---

## 9.6 Construction

Responsible for:

- Work packages
- Construction activities
- Site execution
- Resources
- Progress
- Installation
- Testing
- Punch lists

---

## 9.7 Quality

Responsible for:

- Inspections
- Tests
- Quality records
- NCRs
- Corrective actions
- Quality approvals

---

## 9.8 HSE

Responsible for:

- Safety
- Health
- Environment
- Incidents
- Observations
- Inspections
- Corrective actions

---

## 9.9 Planning and Scheduling

Responsible for:

- Project schedules
- Activities
- Milestones
- Dependencies
- Baselines
- Progress
- Forecast dates
- Delay analysis

---

## 9.10 Cost Management

Responsible for:

- Budget
- Planned cost
- Committed cost
- Actual cost
- Forecast
- Variance

---

## 9.11 Contract Management

Responsible for:

- Client contracts
- Subcontracts
- Contract scope
- Contract value
- Milestones
- Variations
- Claims
- Contract documents

---

## 9.12 Document Control

Responsible for:

- Document registration
- Document numbering
- Revision control
- Review
- Approval
- Distribution
- Document history

---

## 9.13 Inspection and Testing

Responsible for:

- Inspection requests
- Inspection plans
- Test records
- Factory inspections
- Site inspections
- Acceptance tests

---

## 9.14 Commissioning

Responsible for verifying that completed systems are ready for operation.

---

# 10. Business Actors

## 10.1 Client

The organization receiving the completed project.

## 10.2 Project Manager

Responsible for overall project execution.

## 10.3 Engineering User

Responsible for engineering activities and technical deliverables.

## 10.4 Procurement User

Responsible for procurement processes.

## 10.5 Vendor

External organization providing materials or services.

## 10.6 Construction User

Responsible for site execution and construction activities.

## 10.7 Quality User

Responsible for inspections, tests, NCRs, and quality records.

## 10.8 HSE User

Responsible for health, safety, and environmental activities.

## 10.9 Planner / Project Controls User

Responsible for schedules, progress, forecasting, and project controls.

## 10.10 Cost Controller

Responsible for monitoring project costs.

## 10.11 Document Controller

Responsible for project document control.

## 10.12 Management

Requires high-level visibility into:

- Projects
- Costs
- Schedule
- Procurement
- Quality
- HSE
- Risks
- Performance

## 10.13 System Administrator

Responsible for:

- Users
- Roles
- Permissions
- Configuration
- Workflows
- System administration

---

# 11. Major Business Entities

These are conceptual business entities.

They are **not yet Frappe DocTypes**.

Detailed DocType design will be defined later.

---

## 11.1 Organization

Represents an organization participating in the system.

An organization may act as:

- EPC contractor
- Client
- Vendor
- Supplier
- Subcontractor
- Consultant

---

## 11.2 Client

Represents the organization for whom a project is executed.

---

## 11.3 Project

Represents an EPC project.

Possible information:

- Project ID
- Project name
- Client
- Location
- Project type
- Contract
- Start date
- Completion date
- Status
- Project manager

---

## 11.4 Contract

Represents a contractual relationship associated with a project.

---

## 11.5 Project Phase

Represents a major phase of the project.

Examples:

- Engineering
- Procurement
- Construction
- Commissioning
- Handover

---

## 11.6 Engineering Deliverable

Represents an engineering output.

Examples:

- Drawing
- Specification
- Calculation
- Datasheet
- Technical report

---

## 11.7 Engineering Document

Represents a controlled project document.

Possible information:

- Document number
- Revision
- Status
- Project
- Discipline
- Author
- Reviewer
- Approver

---

## 11.8 Material

Represents a physical material required by a project.

---

## 11.9 Equipment

Represents equipment required for a project.

---

## 11.10 Material Requirement

Represents a requirement for material or equipment.

---

## 11.11 Vendor

Represents an external organization supplying goods or services.

---

## 11.12 Purchase Requisition

Represents an internal request to procure goods or services.

---

## 11.13 Request for Quotation

Represents a request sent to vendors for quotations.

---

## 11.14 Vendor Quotation

Represents a quotation received from a vendor.

---

## 11.15 Technical Evaluation

Represents technical assessment of a vendor quotation or proposal.

---

## 11.16 Commercial Evaluation

Represents commercial assessment of vendor offers.

---

## 11.17 Purchase Order

Represents an approved commercial order issued to a vendor.

---

## 11.18 Delivery

Represents delivery of purchased materials, equipment, or services.

---

## 11.19 Material Receipt

Represents receipt of delivered materials or equipment.

---

## 11.20 Construction Activity

Represents a unit of construction work.

---

## 11.21 Work Package

Represents a logical grouping of construction or project activities.

---

## 11.22 Inspection

Represents an inspection performed on:

- Materials
- Equipment
- Engineering outputs
- Construction work

---

## 11.23 Test Record

Represents the result of a project-related test.

---

## 11.24 Non-Conformance Report

Represents a formally identified condition where a requirement has not been satisfied.

---

## 11.25 Corrective Action

Represents an action taken to address an issue or non-conformance.

---

## 11.26 HSE Incident

Represents a health, safety, or environmental incident.

---

## 11.27 HSE Observation

Represents a safety or environmental observation.

---

## 11.28 Project Schedule

Represents the planned project timeline.

---

## 11.29 Schedule Activity

Represents an individual scheduled activity.

---

## 11.30 Milestone

Represents an important planned or achieved point in the project.

---

## 11.31 Project Budget

Represents planned financial allocation.

---

## 11.32 Project Cost

Represents:

- Planned cost
- Committed cost
- Actual cost
- Forecast cost

---

## 11.33 Project Risk

Represents a potential event or condition that could affect project objectives.

---

## 11.34 Project Issue

Represents an identified problem requiring resolution.

---

## 11.35 Change Request

Represents a requested change to:

- Scope
- Design
- Schedule
- Cost
- Other controlled project information

---

## 11.36 Variation

Represents an approved change to contractual or project scope.

---

## 11.37 Commissioning Activity

Represents an activity required to verify system readiness.

---

## 11.38 Handover Package

Represents the collection of documents and records required for project handover.

---

# 12. High-Level Entity Relationships

```text
Organization
    │
    ├── Client
    │
    ├── Vendor
    │
    └── Subcontractor

Client
    │
    ▼
Project
    │
    ├── Contract
    │
    ├── Project Phase
    │
    ├── Engineering
    │      └── Engineering Documents
    │
    ├── Procurement
    │      ├── Material Requirement
    │      ├── Purchase Requisition
    │      ├── RFQ
    │      ├── Vendor Quotation
    │      ├── Technical Evaluation
    │      ├── Commercial Evaluation
    │      ├── Purchase Order
    │      └── Delivery
    │
    ├── Construction
    │      ├── Work Package
    │      └── Construction Activity
    │
    ├── Quality
    │      ├── Inspection
    │      ├── Test Record
    │      ├── NCR
    │      └── Corrective Action
    │
    ├── HSE
    │      ├── HSE Incident
    │      └── HSE Observation
    │
    ├── Planning
    │      ├── Project Schedule
    │      ├── Schedule Activity
    │      └── Milestone
    │
    ├── Cost
    │      ├── Project Budget
    │      └── Project Cost
    │
    ├── Risk
    │      └── Project Risk
    │
    ├── Change Management
    │      ├── Change Request
    │      └── Variation
    │
    ├── Commissioning
    │      └── Commissioning Activity
    │
    └── Handover
           └── Handover Package
```

This is a conceptual model only.

Detailed relationships and cardinality will be designed later.

---

# 13. Core Business Processes

## 13.1 Project Management

```text
Project Initiation
       ↓
Project Planning
       ↓
Project Execution
       ↓
Project Monitoring
       ↓
Project Control
       ↓
Project Completion
       ↓
Project Closure
```

---

## 13.2 Engineering

```text
Engineering Requirement
       ↓
Engineering Planning
       ↓
Design / Engineering
       ↓
Internal Review
       ↓
Client Review
       ↓
Approval
       ↓
Issue for Execution
       ↓
Revision if Required
```

---

## 13.3 Procurement

```text
Requirement
    ↓
Purchase Requisition
    ↓
RFQ
    ↓
Vendor Quotation
    ↓
Technical Evaluation
    ↓
Commercial Evaluation
    ↓
Approval
    ↓
Purchase Order
    ↓
Vendor Execution
    ↓
Inspection
    ↓
Shipment
    ↓
Delivery
    ↓
Receipt
```

---

## 13.4 Construction

```text
Construction Planning
       ↓
Work Package
       ↓
Resource Allocation
       ↓
Construction Execution
       ↓
Progress Recording
       ↓
Inspection
       ↓
Testing
       ↓
Punch List
       ↓
Completion
```

---

## 13.5 Quality

```text
Quality Requirement
       ↓
Inspection Planning
       ↓
Inspection
       ↓
Testing
       ↓
Result
       ↓
Acceptance / Rejection
       ↓
NCR if Required
       ↓
Corrective Action
       ↓
Verification
       ↓
Closure
```

---

## 13.6 HSE

```text
HSE Planning
      ↓
Site Execution
      ↓
Observation / Inspection
      ↓
Incident if Applicable
      ↓
Investigation
      ↓
Corrective Action
      ↓
Verification
      ↓
Closure
```

---

## 13.7 Cost

```text
Project Budget
      ↓
Commitments
      ↓
Actual Costs
      ↓
Cost Monitoring
      ↓
Variance Analysis
      ↓
Forecast
      ↓
Management Reporting
```

---

## 13.8 Schedule

```text
Project Planning
      ↓
Schedule Creation
      ↓
Activity Assignment
      ↓
Baseline
      ↓
Actual Progress
      ↓
Schedule Monitoring
      ↓
Variance Analysis
      ↓
Forecast
```

---

# 14. Business Rules

## BR-001 — Unique Project

Every project must have a unique project identity.

## BR-002 — Project Association

Project-related transactions should be associated with the relevant project where project context is required.

## BR-003 — Controlled Documents

Controlled documents must maintain revision and status information.

## BR-004 — Approval Control

Transactions requiring approval must not be considered approved until the required approval process is completed.

## BR-005 — Procurement Traceability

Procurement transactions should be traceable from requirement to purchase and delivery.

## BR-006 — Vendor Traceability

Vendor-related procurement transactions must identify the relevant vendor.

## BR-007 — Material Traceability

Material transactions should provide traceability from requirement through delivery and receipt where applicable.

## BR-008 — Status Control

Business documents must follow valid status transitions.

## BR-009 — Auditability

Important business transactions must record sufficient history to determine:

- Who performed the action
- What action was performed
- When it was performed
- What changed

## BR-010 — Role-Based Access

Users should only perform actions allowed by their responsibilities and permissions.

## BR-011 — Project Cost Association

Project-related costs should be associated with the relevant project.

## BR-012 — Quality Traceability

Quality records should be traceable to the relevant project, material, equipment, activity, or document where applicable.

## BR-013 — HSE Traceability

HSE records should be associated with the relevant project and context.

## BR-014 — Change Control

Controlled project information should not be modified without appropriate change control after it reaches a controlled state.

## BR-015 — Data Consistency

The system should minimize duplicate master data and inconsistent records.

---

# 15. Business Data

## 15.1 Master Data

Examples:

- Organizations
- Clients
- Vendors
- Materials
- Equipment
- Units of measure
- Locations
- Departments
- Employees
- Users
- Project types
- Categories

---

## 15.2 Project Data

Examples:

- Projects
- Contracts
- Project phases
- Work packages
- Milestones
- Project teams
- Project locations

---

## 15.3 Engineering Data

Examples:

- Engineering documents
- Drawings
- Specifications
- Calculations
- Datasheets
- Technical reports
- Revisions

---

## 15.4 Procurement Data

Examples:

- Material requirements
- Purchase requisitions
- RFQs
- Vendor quotations
- Evaluations
- Purchase orders
- Delivery records

---

## 15.5 Construction Data

Examples:

- Work packages
- Activities
- Progress
- Resources
- Site records
- Completion records

---

## 15.6 Quality Data

Examples:

- Inspections
- Tests
- NCRs
- Corrective actions
- Quality approvals

---

## 15.7 HSE Data

Examples:

- Incidents
- Observations
- Inspections
- Corrective actions
- Safety records

---

## 15.8 Planning Data

Examples:

- Schedules
- Activities
- Dependencies
- Baselines
- Actual dates
- Progress
- Forecast dates

---

## 15.9 Cost Data

Examples:

- Budgets
- Commitments
- Actual costs
- Forecasts
- Variances

---

## 15.10 Document Data

Examples:

- Document metadata
- Files
- Revisions
- Review status
- Approval status
- Distribution records

---

# 16. Business Inputs and Outputs

## 16.1 Major Inputs

The system may receive information from:

- Clients
- Internal project teams
- Engineering teams
- Procurement teams
- Vendors
- Subcontractors
- Construction teams
- Quality teams
- HSE teams
- Finance
- External systems

---

## 16.2 Major Outputs

The system should eventually produce:

- Project dashboards
- Project status reports
- Engineering progress reports
- Procurement reports
- Vendor performance reports
- Material status reports
- Construction progress reports
- Quality reports
- HSE reports
- Cost reports
- Schedule reports
- Risk reports
- Management dashboards
- Handover documentation

---

# 17. Domain Boundaries

## 17.1 Project Domain

Responsible for:

- Projects
- Contracts
- Project teams
- Project phases
- Project status

## 17.2 Engineering Domain

Responsible for:

- Engineering requirements
- Engineering deliverables
- Technical documents
- Engineering revisions

## 17.3 Procurement Domain

Responsible for:

- Requirements
- RFQs
- Quotations
- Evaluations
- Purchase orders
- Procurement tracking

## 17.4 Vendor Domain

Responsible for:

- Vendor master
- Vendor qualification
- Vendor performance
- Vendor documentation

## 17.5 Construction Domain

Responsible for:

- Work packages
- Construction activities
- Progress
- Site execution

## 17.6 Quality Domain

Responsible for:

- Inspections
- Tests
- NCRs
- Corrective actions

## 17.7 HSE Domain

Responsible for:

- Safety
- Health
- Environmental records
- Incidents
- Observations

## 17.8 Project Controls Domain

Responsible for:

- Planning
- Scheduling
- Cost
- Progress
- Forecasting

## 17.9 Document Control Domain

Responsible for:

- Documents
- Revisions
- Reviews
- Approvals
- Distribution
- Traceability

---

# 18. Cross-Domain Relationships

## 18.1 Engineering → Procurement

```text
Engineering
     ↓
Material / Equipment Requirement
     ↓
Procurement
```

---

## 18.2 Procurement → Construction

```text
Procurement
     ↓
Material / Equipment Delivery
     ↓
Construction
```

---

## 18.3 Engineering → Construction

```text
Engineering
     ↓
Approved Design
     ↓
Construction
```

---

## 18.4 Construction → Quality

```text
Construction
     ↓
Inspection / Testing
     ↓
Quality
```

---

## 18.5 Construction → HSE

```text
Construction
     ↓
HSE Monitoring
     ↓
Observation / Incident / Corrective Action
```

---

## 18.6 All Domains → Project Controls

```text
Engineering ─────┐
Procurement ─────┤
Construction ────┤
Quality ─────────┤
HSE ─────────────┤
Cost ────────────┤
                 ▼
          Project Controls
                 │
                 ▼
        Management Reporting
```

---

# 19. Overall Information Flow

```text
CLIENT REQUIREMENT
        ↓
PROJECT
        ↓
CONTRACT / SCOPE
        ↓
PROJECT PLANNING
        ↓
ENGINEERING REQUIREMENTS
        ↓
ENGINEERING DELIVERABLES
        ↓
MATERIAL / EQUIPMENT REQUIREMENTS
        ↓
PROCUREMENT
        ↓
VENDOR
        ↓
PURCHASE
        ↓
DELIVERY
        ↓
CONSTRUCTION
        ↓
QUALITY + HSE
        ↓
TESTING
        ↓
COMMISSIONING
        ↓
HANDOVER
```

Cross-cutting processes:

```text
Documents
Approvals
Cost
Schedule
Risk
Quality
HSE
Change Management
Communication
```

---

# 20. Core Business Principles

## 20.1 Single Source of Truth

The ERP should provide a reliable central source for controlled business information.

## 20.2 Process Integration

Business processes should be connected instead of isolated.

## 20.3 Traceability

Important transactions should be traceable across their lifecycle.

## 20.4 Controlled Changes

Changes to controlled information should follow defined processes.

## 20.5 Role-Based Responsibility

Users should access and modify information according to their responsibilities.

## 20.6 Auditability

Important business actions should be traceable.

## 20.7 Data Consistency

Master and transactional data should remain consistent.

## 20.8 Workflow-Based Execution

Important business processes should use defined workflows.

## 20.9 Extensibility

The system should support future EPC-specific extensions.

## 20.10 Integration

The platform should be capable of integrating with external systems when required.

---

# 21. ERPNext and Frappe Strategy

The system will be developed using:

```text
ERPNext
    ↓
Frappe Framework
    ↓
Custom EPC Application
```

The development strategy is:

```text
Business Requirement
        ↓
Domain Analysis
        ↓
Process Design
        ↓
ERPNext Capability Mapping
        ↓
Reuse Standard ERPNext
        ↓
Identify Gaps
        ↓
Custom Frappe Development
```

The system should avoid unnecessary custom development.

Where ERPNext already provides suitable functionality, standard ERPNext capabilities should be preferred.

Custom development should be introduced when:

- The business process is EPC-specific.
- Standard ERPNext functionality does not satisfy the requirement.
- A required workflow cannot be represented appropriately.
- Additional business rules are required.
- EPC-specific reporting or dashboards are required.
- Additional integrations are required.

---

# 22. Future Digital Transformation

The system should provide a foundation for future digital capabilities.

The expected maturity path is:

```text
Transaction Management
        ↓
Workflow Automation
        ↓
Operational Visibility
        ↓
Reporting
        ↓
Analytics
        ↓
Predictive Analytics
        ↓
AI-Assisted Decision Support
```

Potential future capabilities:

- Automated notifications
- Automated approvals
- Procurement alerts
- Vendor performance analytics
- Project delay prediction
- Cost forecasting
- Risk prediction
- Document intelligence
- AI-assisted search
- AI-assisted project reporting

These capabilities are future possibilities and are not part of the initial implementation unless separately approved.

---

# 23. Assumptions

## ASSUMPTION-001

The system initially targets a general EPC business model.

## ASSUMPTION-002

ERPNext standard functionality will be reused wherever it satisfies the business requirement.

## ASSUMPTION-003

Custom Frappe development will be used for EPC-specific requirements.

## ASSUMPTION-004

The system will support multiple projects.

## ASSUMPTION-005

Projects may involve multiple departments and business processes.

## ASSUMPTION-006

Users may participate in different processes according to their responsibilities.

## ASSUMPTION-007

Sector-specific extensions may be added after the general EPC model is validated.

## ASSUMPTION-008

Existing ERPNext capabilities will be evaluated before creating custom functionality.

## ASSUMPTION-009

Business workflows may vary depending on:

- Contract type
- Project type
- Client requirements
- Organization policies
- Regulatory requirements

---

# 24. Constraints

Potential constraints include:

- EPC sectors have different processes.
- Client requirements may vary between projects.
- Contract requirements may affect workflows.
- Regulatory requirements may vary by location and industry.
- Existing systems may need integration.
- Large projects may generate significant document volumes.
- Users may have different technical skills.
- Some project information may be confidential.
- External vendors may require restricted access.
- Existing organizational processes may need to be preserved during migration.

---

# 25. Open Questions

The following questions must be answered before detailed implementation design.

## Business Scope

1. Which EPC sector is the primary target?
2. Is the target Oil & Gas, Power, Solar, Industrial, Infrastructure, or multiple sectors?
3. Is the system for one EPC organization or multiple organizations?
4. How many projects should the system support?

## Project Management

5. What project lifecycle does the organization currently follow?
6. What project phases are mandatory?
7. What project statuses are required?

## Engineering

8. Which engineering disciplines must be supported?
9. What engineering document types are required?
10. How are engineering documents reviewed?
11. How are engineering documents approved?
12. How are revisions controlled?

## Procurement

13. What is the procurement approval workflow?
14. How are vendors selected?
15. Is technical evaluation mandatory?
16. Is commercial evaluation mandatory?
17. How are purchase orders approved?

## Vendor Management

18. How are vendors registered?
19. Is vendor qualification required?
20. How is vendor performance measured?

## Construction

21. How is construction work divided?
22. What is the organization's definition of a work package?
23. How is construction progress calculated?
24. How are site activities recorded?

## Quality

25. What inspection processes are required?
26. How are NCRs managed?
27. What quality documents must be maintained?

## HSE

28. What HSE processes are mandatory?
29. How are incidents recorded?
30. What safety inspections are required?

## Planning

31. What scheduling methodology is used?
32. What scheduling software is currently used?
33. How is project progress measured?

## Cost

34. How is project cost tracked?
35. What cost categories are required?
36. How are cost forecasts calculated?

## Contracts

37. What contract types are used?
38. How are variations managed?
39. How are claims managed?

## Documents

40. What document management system currently exists?
41. What document numbering convention is used?
42. What revision rules are required?
43. What approval rules are required?

## ERPNext

44. Which ERPNext modules can be reused?
45. Which ERPNext DocTypes already cover the requirements?
46. Which requirements need custom DocTypes?
47. Which requirements need custom workflows?
48. Which external systems need integration?

---

# 26. Domain Model Maturity

This document represents the **initial conceptual business model**.

The design will evolve through:

```text
Business Understanding
        ↓
Domain Analysis
        ↓
Business Requirements
        ↓
Functional Requirements
        ↓
Use Cases
        ↓
Business Process Design
        ↓
Workflow Design
        ↓
Domain Model Refinement
        ↓
ER Model
        ↓
ERPNext Mapping
        ↓
Technical Architecture
        ↓
Frappe Implementation
        ↓
Testing
        ↓
Deployment
```

---

# 27. Current Project State

At the time of creating this document, the project is in the:

**Pre-Development / Requirements & System Design Phase**

Current focus:

```text
Understand EPC Domain
        ↓
Document Business Requirements
        ↓
Document Business Processes
        ↓
Design Domain Model
        ↓
Design System
        ↓
Map Requirements to ERPNext
        ↓
Identify Custom Frappe Requirements
        ↓
Development
```

Development should begin only after the required design and documentation have been sufficiently reviewed.

---

# 28. Document Status

**Document:** 00_Business_Requirements_and_Domain_Model.md

**Purpose:** Establish the initial business and domain foundation.

**Current Status:** Draft

**Next Documents:** The subsequent design documents will progressively define the detailed requirements, processes, architecture, data model, ERPNext mapping, Frappe customization, workflows, UI, security, testing, deployment, and operational design.

---

# 29. Final Domain Summary

The EPC ERP System is intended to become an integrated platform for managing the complete EPC project lifecycle.

The core relationship is:

```text
                    CLIENT
                       ↓
                    PROJECT
                       ↓
              ┌────────┴────────┐
              ↓                 ↓
         ENGINEERING       PROCUREMENT
              ↓                 ↓
              └────────┬────────┘
                       ↓
                  CONSTRUCTION
                       ↓
             ┌─────────┴─────────┐
             ↓                   ↓
          QUALITY               HSE
             │                   │
             └─────────┬─────────┘
                       ↓
                PROJECT CONTROLS
                       ↓
                 COMMISSIONING
                       ↓
                    HANDOVER
                       ↓
                     CLIENT
```

The system will use **ERPNext + Frappe Framework** as the foundation and will add custom EPC-specific capabilities where standard ERPNext functionality is insufficient.

The immediate priority is not coding.

The immediate priority is to **understand, document, validate, and design the EPC business domain before development begins**.