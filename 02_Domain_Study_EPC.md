# 02 — Domain Study: Engineering, Procurement & Construction (EPC)

**Project:** EPC ERP System  
**Domain:** Engineering, Procurement & Construction  
**Platform:** ERPNext + Frappe Framework  
**Document Type:** Domain Study  
**Document Status:** Draft  
**Version:** 1.0  
**Current Phase:** Pre-Development / Domain Understanding

---

## 1. Purpose of This Document

This document provides a detailed study of the Engineering, Procurement & Construction (EPC) domain before software development begins.

The purpose is to understand how an EPC organization actually executes projects, what departments are involved, how business processes are connected, what information flows between departments, and what an ERP system needs to represent.

This document is a domain-understanding document.

It is not yet a final software design.

The objective is to understand the real-world business first and convert that understanding into software requirements later.

The overall approach is:

**Understand the Domain → Understand the Processes → Identify Business Objects → Identify Relationships → Identify Requirements → Design the ERP System**

---

# 2. What Is EPC?

EPC stands for:

**Engineering, Procurement & Construction**

EPC is a project delivery model commonly used for large and complex projects.

In an EPC project, an organization is responsible for performing or coordinating major activities required to design, procure, construct, test, commission, and hand over a facility or project to a client.

At a high level:

**Engineering**

Design the facility, systems, equipment, and technical solution.

**Procurement**

Purchase or arrange the materials, equipment, and services required to execute the project.

**Construction**

Build, install, assemble, and execute the physical project.

These three areas are strongly interconnected.

A simplified relationship is:

**Engineering → Procurement → Construction**

However, real EPC projects are more complex because these activities often overlap.

Engineering may continue while procurement is already taking place.

Procurement may continue while construction has already started.

Construction may begin for some areas while engineering is still being completed for other areas.

Therefore, EPC should be understood as an integrated project execution system rather than three completely separate departments.

---

# 3. EPC in Simple Terms

A simple way to understand EPC is:

A client wants a facility or project.

For example:

- Power plant
- Oil and gas facility
- Chemical plant
- Manufacturing facility
- Water treatment plant
- Infrastructure project
- Industrial facility
- Building or large construction project

The client defines what they need.

The EPC organization then has to:

1. Understand the client's requirements.
2. Plan the project.
3. Design the solution.
4. Determine what materials and equipment are required.
5. Purchase those materials and equipment.
6. Construct the facility.
7. Inspect and test the work.
8. Commission the completed systems.
9. Prepare project documentation.
10. Hand over the completed project to the client.

Therefore:

**Client Requirement → Engineering → Procurement → Construction → Commissioning → Handover**

---

# 4. EPC Project Lifecycle

A simplified EPC lifecycle is:

**Opportunity / Contract Award**

↓

**Project Initiation**

↓

**Project Planning**

↓

**Engineering**

↓

**Procurement**

↓

**Construction**

↓

**Testing & Inspection**

↓

**Commissioning**

↓

**Handover**

↓

**Project Closure**

However, the actual lifecycle is not strictly sequential.

Several activities occur simultaneously.

For example:

**Engineering**
→ Design development

**Procurement**
→ Vendor sourcing and purchasing

**Construction**
→ Site execution

These can all happen at the same time.

---

# 5. Why EPC Projects Are Complex

EPC projects are complex because they combine many different business disciplines.

A single project may involve:

- Client
- Project management
- Engineering
- Procurement
- Vendors
- Suppliers
- Construction teams
- Subcontractors
- Quality teams
- HSE teams
- Planning teams
- Cost control teams
- Document control teams
- Finance
- Legal
- Contracts
- Commissioning teams
- Operations teams

Each department produces information that another department may need.

For example:

Engineering produces an equipment specification.

↓

Procurement uses that specification to request quotations.

↓

A vendor supplies the equipment.

↓

Quality inspects the equipment.

↓

Construction installs the equipment.

↓

Commissioning tests the equipment.

Therefore, the same equipment may appear across multiple business processes.

This creates a strong requirement for integration and traceability.

---

# 6. Main EPC Domains

The major domains involved in an EPC organization include:

1. Business Development
2. Contract Management
3. Project Management
4. Engineering
5. Procurement
6. Vendor Management
7. Material Management
8. Logistics
9. Construction
10. Quality Management
11. HSE Management
12. Planning & Scheduling
13. Cost Control
14. Risk Management
15. Change Management
16. Document Control
17. Commissioning
18. Project Handover
19. Finance
20. Human Resources
21. Asset Management
22. Reporting and Analytics

Not every EPC company will organize these areas in exactly the same way.

The structure may vary depending on:

- Industry
- Project size
- Contract type
- Country
- Client requirements
- Company structure
- Regulatory environment

---

# 7. Business Development

Business Development happens before a project becomes an active execution project.

Typical activities include:

- Identifying opportunities
- Receiving client requirements
- Studying tender documents
- Preparing technical proposals
- Preparing commercial proposals
- Estimating project cost
- Estimating project duration
- Preparing bids
- Negotiating with clients
- Contract award

Simplified flow:

**Opportunity → Tender → Proposal → Negotiation → Contract Award**

Once the contract is awarded, the project moves into execution.

---

# 8. Contract Management

The contract defines the commercial and contractual relationship between the client and the EPC organization.

Important information may include:

- Contract number
- Client
- Project
- Contract value
- Currency
- Contract scope
- Start date
- Completion date
- Payment terms
- Milestones
- Deliverables
- Contract obligations
- Performance requirements
- Change provisions
- Claims
- Variations
- Penalties
- Warranties

Contract management is important because project execution must remain aligned with contractual commitments.

---

# 9. Project Management

Project Management coordinates the overall EPC project.

The Project Manager is responsible for ensuring that the project is executed according to:

- Scope
- Schedule
- Cost
- Quality
- Safety
- Contract requirements

A simplified project management model is:

**Scope + Time + Cost + Quality + Safety**

The Project Manager needs information from almost every department.

For example:

- Engineering progress
- Procurement progress
- Construction progress
- Cost performance
- Schedule performance
- Quality issues
- HSE incidents
- Risks
- Change requests

Therefore, the Project Management domain becomes a central integration point.

---

# 10. Engineering

Engineering converts client requirements into technical designs and specifications.

Engineering may include multiple disciplines.

Common disciplines include:

- Process Engineering
- Mechanical Engineering
- Civil Engineering
- Structural Engineering
- Piping Engineering
- Electrical Engineering
- Instrumentation Engineering
- Architectural Engineering
- Environmental Engineering
- Specialized engineering disciplines

Engineering produces technical information required by procurement and construction.

---

# 11. Engineering Deliverables

Engineering deliverables can include:

- Drawings
- Specifications
- Datasheets
- Calculations
- Design reports
- Technical reports
- Equipment specifications
- Material specifications
- Layouts
- Engineering schedules
- Technical documents
- Design models
- As-built drawings

These deliverables must often go through review and approval processes.

---

# 12. Engineering Document Lifecycle

A simplified engineering document lifecycle is:

**Create**

↓

**Internal Review**

↓

**Submit**

↓

**Client Review**

↓

**Approved / Approved with Comments / Rejected**

↓

**Revise**

↓

**Resubmit**

↓

**Approved**

↓

**Issued for Construction**

The exact statuses depend on the project and client requirements.

This is why document revision management is extremely important in EPC systems.

---

# 13. Engineering and Procurement Relationship

Engineering determines what needs to be purchased.

For example:

Engineering identifies:

**Pump**

↓

Defines:

- Capacity
- Pressure
- Temperature
- Material
- Motor requirements
- Technical standards

↓

Procurement uses this information to source the equipment.

Therefore:

**Engineering Requirement → Procurement Requirement**

If engineering changes the specification after procurement has started, procurement may also need to change.

This creates a dependency between the two domains.

---

# 14. Procurement

Procurement is responsible for obtaining the goods and services required for project execution.

Procurement may include:

- Material sourcing
- Equipment purchasing
- Service procurement
- Vendor selection
- Commercial evaluation
- Purchase orders
- Delivery tracking
- Expediting
- Inspection coordination
- Logistics coordination

The procurement process generally begins with a requirement.

---

# 15. Procurement Lifecycle

A simplified procurement lifecycle is:

**Requirement**

↓

**Purchase Requisition**

↓

**Request for Quotation**

↓

**Vendor Quotations**

↓

**Technical Evaluation**

↓

**Commercial Evaluation**

↓

**Vendor Selection**

↓

**Approval**

↓

**Purchase Order**

↓

**Manufacturing / Preparation**

↓

**Inspection**

↓

**Shipment**

↓

**Delivery**

↓

**Receipt**

↓

**Material Availability**

This process should ideally be traceable within the ERP system.

---

# 16. Purchase Requisition

A Purchase Requisition represents an internal request to obtain a material, equipment item, or service.

It may contain:

- Project
- Requester
- Required date
- Item
- Quantity
- Unit
- Technical specification
- Required location
- Priority
- Cost estimate
- Supporting documents

The requisition may require approval before procurement can proceed.

---

# 17. Request for Quotation

An RFQ is a request sent to one or more vendors asking them to provide commercial and technical information.

It may contain:

- Item
- Quantity
- Specification
- Delivery requirement
- Terms
- Required documents
- Technical requirements

Multiple vendors may receive the same RFQ.

---

# 18. Vendor Quotation

A vendor quotation may contain:

- Vendor
- Price
- Currency
- Quantity
- Delivery time
- Payment terms
- Warranty
- Technical information
- Exceptions
- Commercial conditions

The procurement team may compare multiple quotations.

---

# 19. Technical Evaluation

Technical evaluation determines whether a vendor's offering satisfies the engineering and technical requirements.

Possible result:

**Technically Acceptable**

or

**Technically Not Acceptable**

Technical evaluation may involve Engineering and Procurement together.

This is an important cross-department workflow.

---

# 20. Commercial Evaluation

Commercial evaluation compares factors such as:

- Price
- Payment terms
- Delivery
- Warranty
- Taxes
- Freight
- Commercial conditions
- Total cost

The final vendor selection may depend on both technical and commercial evaluation.

---

# 21. Purchase Order

A Purchase Order is the formal order issued to a vendor.

It may contain:

- Vendor
- Project
- Items
- Quantities
- Prices
- Delivery dates
- Terms and conditions
- Technical references
- Payment terms
- Shipping information

The Purchase Order becomes an important transaction for procurement, finance, logistics, and project cost control.

---

# 22. Vendor Management

Vendors are external organizations that provide:

- Materials
- Equipment
- Services
- Subcontracting
- Specialized work

Vendor management may include:

- Vendor registration
- Vendor qualification
- Vendor approval
- Vendor evaluation
- Vendor performance
- Vendor documents
- Vendor history

The system should maintain reliable vendor master data.

---

# 23. Vendor Performance

Vendor performance may be evaluated using:

- Quality
- Delivery performance
- Cost
- Responsiveness
- Technical compliance
- Documentation quality
- HSE performance

Possible KPIs include:

- On-time delivery percentage
- Rejection rate
- NCR count
- Average delivery delay
- Response time

This information can later support analytics.

---

# 24. Material Management

Materials are central to EPC execution.

Materials may include:

- Pipes
- Valves
- Pumps
- Motors
- Cables
- Steel
- Electrical equipment
- Instrumentation
- Construction materials
- Spare parts
- Specialized equipment

Material management tracks what is required, ordered, received, inspected, stored, issued, and consumed.

---

# 25. Material Lifecycle

A simplified material lifecycle is:

**Material Requirement**

↓

**Procurement**

↓

**Purchase Order**

↓

**Manufacturing / Supply**

↓

**Shipment**

↓

**Receipt**

↓

**Inspection**

↓

**Storage**

↓

**Issue to Construction**

↓

**Installation**

↓

**Consumption / Asset**

This creates relationships between Engineering, Procurement, Inventory, Quality, and Construction.

---

# 26. Logistics

Logistics manages movement of materials and equipment.

It may involve:

- Shipment planning
- Transportation
- Freight
- Customs
- Delivery tracking
- Shipping documents
- Warehousing
- Site delivery

For international EPC projects, logistics can become a major part of project execution.

---

# 27. Construction

Construction is the physical execution phase of the project.

Activities may include:

- Site preparation
- Civil works
- Structural works
- Equipment installation
- Piping
- Electrical installation
- Instrumentation
- Mechanical installation
- Testing
- Finishing
- Completion

Construction depends heavily on:

- Engineering information
- Material availability
- Equipment availability
- Workforce
- Planning
- Quality
- HSE

---

# 28. Construction Work Packages

Construction work may be divided into manageable work packages.

A work package may contain:

- Project
- Area
- Discipline
- Scope
- Activities
- Materials
- Resources
- Planned dates
- Actual dates
- Progress
- Quality requirements
- HSE requirements

This allows construction progress to be measured systematically.

---

# 29. Construction Progress

Construction progress can be measured using:

- Activities completed
- Quantities installed
- Work packages completed
- Milestones achieved
- Percentage completion

Example:

Planned quantity:

100 meters of pipe

Installed quantity:

60 meters

Progress:

60%

The exact progress measurement method depends on the project.

---

# 30. Quality Management

Quality Management ensures that project work satisfies required standards and specifications.

Quality activities may include:

- Inspection
- Testing
- Quality planning
- Material inspection
- Construction inspection
- Document review
- Non-Conformance Management
- Corrective actions

Quality should be integrated into the project lifecycle rather than treated as a separate activity at the end.

---

# 31. Inspection and Test Plan

An Inspection and Test Plan defines:

- What must be inspected
- What must be tested
- When it must be inspected
- Who is responsible
- Acceptance criteria
- Required documentation

Typical participants may include:

- Contractor
- EPC organization
- Third-party inspector
- Client

---

# 32. Non-Conformance Report

An NCR is raised when work, material, or a deliverable does not meet the required specification or standard.

Simplified lifecycle:

**Non-Conformance Identified**

↓

**NCR Created**

↓

**Investigation**

↓

**Root Cause**

↓

**Corrective Action**

↓

**Verification**

↓

**Closure**

NCR management provides important quality traceability.

---

# 33. HSE

HSE stands for:

**Health, Safety and Environment**

HSE is critical in EPC projects because construction and industrial projects can involve significant risks.

HSE activities may include:

- Safety inspections
- Safety observations
- Incident reporting
- Near-miss reporting
- Environmental monitoring
- Risk assessments
- Corrective actions
- Safety training
- Permit management

---

# 34. HSE Incident Management

A simplified incident lifecycle is:

**Incident Occurs**

↓

**Incident Report**

↓

**Investigation**

↓

**Root Cause Analysis**

↓

**Corrective / Preventive Actions**

↓

**Verification**

↓

**Closure**

The system should preserve the history of the incident and associated actions.

---

# 35. Planning and Scheduling

Planning determines:

- What must be done
- When it must be done
- In what order
- By whom
- With what resources

Schedules may contain:

- Activities
- Milestones
- Dependencies
- Start dates
- Finish dates
- Durations
- Baselines
- Actual progress
- Forecast dates

---

# 36. Schedule Dependencies

Activities may depend on other activities.

Example:

Engineering Approval  
→ Procurement  
→ Material Delivery  
→ Construction

If engineering approval is delayed, procurement may be delayed.

If procurement is delayed, construction may be delayed.

Therefore, schedule dependencies are important for project control.

---

# 37. Cost Control

Cost Control tracks project financial performance.

Important concepts include:

- Budget
- Planned Cost
- Committed Cost
- Actual Cost
- Forecast Cost
- Variance

A simplified model is:

**Budget**

→ Planned Cost

→ Commitments

→ Actual Cost

→ Forecast

→ Variance Analysis

---

# 38. Project Budget

A project budget represents the planned financial resources required to execute the project.

Budget categories may include:

- Engineering
- Procurement
- Construction
- Labor
- Equipment
- Materials
- Subcontractors
- Logistics
- Overheads

The actual structure depends on the organization and project.

---

# 39. Committed Cost

Committed cost represents costs that the organization has committed to through transactions such as:

- Purchase Orders
- Subcontracts
- Service Orders

Committed cost is important because actual expenditure may happen later.

Therefore:

**Budget ≠ Actual Cost**

and:

**Budget ≠ Committed Cost**

Both should be monitored.

---

# 40. Risk Management

Every EPC project contains risks.

Examples:

- Engineering delays
- Procurement delays
- Vendor delays
- Material shortages
- Cost increases
- Design changes
- Construction delays
- Quality failures
- HSE incidents
- Regulatory issues
- Weather conditions
- Logistics problems

Risk management identifies and monitors these risks.

---

# 41. Risk Lifecycle

A typical risk lifecycle is:

**Identify**

↓

**Assess**

↓

**Prioritize**

↓

**Assign Owner**

↓

**Mitigation Plan**

↓

**Monitor**

↓

**Review**

↓

**Close / Accept / Escalate**

Risk management should be connected with project planning and decision making.

---

# 42. Change Management

Changes are common in EPC projects.

Changes may happen because of:

- Client requests
- Design changes
- Site conditions
- Regulatory requirements
- Material availability
- Cost changes
- Schedule changes
- Engineering discoveries

A change can affect:

- Scope
- Cost
- Schedule
- Quality
- Procurement
- Construction

Therefore, changes should be controlled.

---

# 43. Change Request Lifecycle

A typical change process is:

**Change Identified**

↓

**Change Request**

↓

**Impact Analysis**

↓

**Technical Review**

↓

**Cost Analysis**

↓

**Schedule Analysis**

↓

**Approval**

↓

**Implementation**

↓

**Verification**

↓

**Closure**

---

# 44. Document Control

EPC projects generate a very large amount of documentation.

Examples:

- Drawings
- Specifications
- Contracts
- Purchase orders
- Vendor documents
- Inspection reports
- Test reports
- Quality documents
- HSE documents
- Construction records
- As-built drawings

Document Control ensures that the correct document and revision are available to the correct users.

---

# 45. Document Revision Management

A document may go through multiple revisions.

Example:

Revision A  
→ Revision B  
→ Revision C  
→ Revision D

Each revision may represent a change in:

- Design
- Specification
- Requirements
- Comments
- Technical information

The system must prevent obsolete revisions from being accidentally used.

---

# 46. Commissioning

Commissioning verifies that installed systems and equipment work correctly.

Commissioning may include:

- System verification
- Equipment testing
- Functional testing
- Performance testing
- Safety verification
- Documentation verification

Construction completion does not necessarily mean the project is operational.

Commissioning provides the transition from construction completion to operational readiness.

---

# 47. Punch List

A punch list contains incomplete or defective items that must be resolved before final completion or handover.

Examples:

- Missing labels
- Incomplete installation
- Documentation missing
- Minor defects
- Testing pending
- Painting incomplete

Punch items should have:

- Description
- Location
- Responsible party
- Priority
- Due date
- Status
- Closure evidence

---

# 48. Project Handover

Handover is the transition from project execution to the client or operational organization.

A handover package may contain:

- As-built drawings
- Test records
- Inspection records
- Certificates
- Equipment documents
- Operation and maintenance manuals
- Quality records
- HSE records
- Punch-list closure evidence

Handover should only occur when defined completion requirements are satisfied.

---

# 49. Project Closure

After handover, the project may move into closure.

Closure may include:

- Final documentation
- Contract closure
- Financial closure
- Final cost
- Lessons learned
- Asset handover
- Final reports
- Archive
- Resource release

The project should retain historical information for future reference and audits.

---

# 50. EPC Information Flow

One of the most important concepts for an EPC ERP system is information flow.

A simplified flow is:

**Client Requirement**

→ Contract

→ Project

→ Engineering

→ Engineering Deliverables

→ Procurement Requirements

→ Purchase Requisition

→ RFQ

→ Vendor Quotation

→ Purchase Order

→ Delivery

→ Inspection

→ Material Receipt

→ Construction

→ Quality

→ Commissioning

→ Handover

This represents an end-to-end business chain.

---

# 51. Cross-Department Dependencies

EPC departments are highly dependent on each other.

### Engineering → Procurement

Engineering provides specifications and technical requirements.

### Procurement → Construction

Procurement provides materials and equipment.

### Engineering → Construction

Engineering provides approved drawings and technical information.

### Quality → Construction

Quality verifies construction activities.

### HSE → Construction

HSE controls safety and environmental requirements.

### Planning → All Departments

Planning coordinates timelines and progress.

### Cost Control → Management

Cost Control provides financial performance information.

### Document Control → All Departments

Document Control ensures controlled project information.

---

# 52. EPC Master Data

Master data is the stable information used across multiple transactions.

Potential EPC master data includes:

- Company
- Client
- Project
- Contract
- Vendor
- Customer
- Employee
- Department
- Discipline
- Material
- Item
- Warehouse
- Location
- Equipment
- Asset
- Unit of Measure
- Currency
- Tax
- Cost Center
- Project Phase

Master data quality is critical because incorrect master data can affect many transactions.

---

# 53. EPC Transaction Data

Transaction data represents business activities occurring during project execution.

Examples:

- Project
- Purchase Requisition
- RFQ
- Vendor Quotation
- Purchase Order
- Material Receipt
- Inspection
- Engineering Deliverable
- NCR
- HSE Incident
- Work Package
- Construction Activity
- Change Request
- Risk
- Punch Item
- Commissioning Record
- Handover Package

Transaction records should reference relevant master data.

---

# 54. Master Data vs Transaction Data

A simple distinction:

**Master Data**

Defines the entities.

Examples:

- Vendor
- Material
- Project
- Employee

**Transaction Data**

Records activities involving those entities.

Examples:

- Purchase Order
- Material Receipt
- Inspection
- Change Request

Relationship:

**Master Data → Used by Transactions**

Good master data is essential for reliable reporting.

---

# 55. EPC Hierarchy

An EPC organization may need multiple levels of project structure.

A simplified hierarchy can be:

**Company**

→ Project

→ Contract

→ Phase

→ Area

→ System

→ Subsystem

→ Work Package

→ Activity

The exact hierarchy depends on the project.

This hierarchy is important when designing the data model.

---

# 56. Project Breakdown Structure

A project may be divided into smaller manageable components.

Examples:

- Project
- Area
- Discipline
- System
- Subsystem
- Work Package
- Activity

This helps with:

- Planning
- Cost tracking
- Progress tracking
- Reporting
- Responsibility assignment

---

# 57. Work Breakdown Structure

WBS means:

**Work Breakdown Structure**

It divides the project scope into smaller work components.

Example:

Project

→ Civil Works

→ Foundation

→ Equipment Foundation

→ Excavation

→ Reinforcement

→ Concrete

Each level provides more detailed control over the work.

---

# 58. Cost Breakdown Structure

CBS means:

**Cost Breakdown Structure**

It organizes project costs into structured categories.

Example:

Project

→ Engineering

→ Procurement

→ Construction

→ Labor

→ Materials

→ Equipment

→ Subcontract

→ Logistics

This allows project cost reporting at different levels.

---

# 59. Organization Structure

The ERP system may also need to represent organizational structure.

Example:

Company

→ Department

→ Team

→ Employee

Departments may include:

- Engineering
- Procurement
- Construction
- Quality
- HSE
- Planning
- Finance
- Contracts
- Document Control

Organizational structure can influence permissions and workflow responsibilities.

---

# 60. Roles in EPC

Different users perform different responsibilities.

Examples:

- Project Manager
- Engineering Manager
- Engineer
- Procurement Manager
- Buyer
- Vendor Coordinator
- Construction Manager
- Site Engineer
- Quality Engineer
- HSE Officer
- Planner
- Cost Controller
- Contract Manager
- Document Controller
- Commissioning Engineer
- Finance User
- System Administrator

The exact software roles should be derived from actual responsibilities rather than created arbitrarily.

---

# 61. EPC Workflow Concept

Many EPC processes require approvals.

Examples:

Purchase Requisition:

**Draft → Submitted → Approved → Rejected**

Engineering Document:

**Draft → Review → Client Review → Approved → Issued**

NCR:

**Open → Investigation → Corrective Action → Verification → Closed**

Change Request:

**Draft → Review → Approval → Implementation → Closed**

Therefore, workflow is a major part of the EPC ERP design.

---

# 62. EPC Traceability

Traceability is one of the most important concepts in the system.

The system should allow users to trace:

**Requirement → Transaction → Result**

For example:

Engineering Requirement

→ Material

→ Purchase Requisition

→ RFQ

→ Vendor

→ Purchase Order

→ Delivery

→ Inspection

→ Receipt

→ Construction

→ Commissioning

→ Handover

This provides end-to-end visibility.

---

# 63. EPC Audit Trail

The system should maintain information about important actions.

Important questions include:

- Who created the record?
- Who modified it?
- Who approved it?
- When was it approved?
- What changed?
- Which revision was used?
- Which project was involved?

This is especially important for controlled documents, contracts, procurement, quality, and approvals.

---

# 64. EPC Reporting Requirements

Different users need different reports.

### Management Reports

- Project portfolio
- Project health
- Cost performance
- Schedule performance
- Major risks
- Major issues

### Engineering Reports

- Deliverable status
- Approval status
- Overdue documents
- Revision status

### Procurement Reports

- PR status
- RFQ status
- PO status
- Vendor performance
- Delivery status

### Construction Reports

- Progress
- Work package status
- Material availability
- Productivity

### Quality Reports

- Inspection status
- NCR status
- Test results

### HSE Reports

- Incidents
- Near misses
- Safety observations
- Corrective actions

---

# 65. EPC Dashboard Concept

A project dashboard should provide a high-level view of project health.

Possible dashboard sections:

### Project

- Overall progress
- Planned completion
- Forecast completion
- Project status

### Engineering

- Deliverables
- Pending approvals
- Overdue documents

### Procurement

- Purchase orders
- Delivery status
- Delayed items

### Construction

- Progress
- Work packages
- Open activities

### Quality

- Inspections
- NCRs
- Open actions

### HSE

- Incidents
- Observations
- Open actions

### Cost

- Budget
- Actual
- Commitment
- Forecast

### Risk

- High risks
- Medium risks
- Open mitigation actions

---

# 66. EPC Data Relationships

Important relationships may include:

**Client → Contract**

**Contract → Project**

**Project → Engineering Deliverables**

**Project → Purchase Requisitions**

**Project → Purchase Orders**

**Project → Vendors**

**Project → Materials**

**Project → Work Packages**

**Project → Risks**

**Project → Change Requests**

**Project → Quality Records**

**Project → HSE Records**

**Project → Commissioning Records**

**Project → Handover Packages**

These relationships will later influence the ERP data model.

---

# 67. EPC as an Integrated System

The most important domain understanding is that EPC should not be designed as isolated modules.

Instead:

**Project**

is the central context.

Around the project:

- Engineering
- Procurement
- Construction
- Quality
- HSE
- Planning
- Cost
- Risk
- Contracts
- Documents
- Commissioning

all interact with each other.

The ERP should represent these relationships.

---

# 68. Example End-to-End Scenario

Consider a project that requires a large pump.

### Step 1 — Engineering

Engineering defines the pump requirements.

### Step 2 — Procurement Requirement

The requirement becomes a procurement requirement.

### Step 3 — Purchase Requisition

Procurement receives the requirement.

### Step 4 — RFQ

The procurement team requests quotations from vendors.

### Step 5 — Vendor Quotations

Several vendors submit quotations.

### Step 6 — Technical Evaluation

Engineering evaluates technical compliance.

### Step 7 — Commercial Evaluation

Procurement evaluates commercial terms.

### Step 8 — Purchase Order

The selected vendor receives the Purchase Order.

### Step 9 — Manufacturing

The vendor manufactures or prepares the pump.

### Step 10 — Inspection

Quality or an inspection agency checks the pump.

### Step 11 — Shipment

The pump is transported to the project site.

### Step 12 — Receipt

The material is received.

### Step 13 — Construction

The pump is installed.

### Step 14 — Testing

The pump is tested.

### Step 15 — Commissioning

The pump is commissioned.

### Step 16 — Handover

The pump and its documentation become part of the project handover.

This single example demonstrates why EPC software requires integration.

---

# 69. What the ERP System Must Understand

From the domain study, the ERP system needs to understand:

### Entities

- Company
- Client
- Project
- Contract
- Vendor
- Employee
- Material
- Equipment
- Document
- Work Package
- Activity

### Processes

- Engineering
- Procurement
- Construction
- Quality
- HSE
- Planning
- Cost Control
- Risk
- Change
- Commissioning
- Handover

### Relationships

- Project to Contract
- Project to Engineering
- Engineering to Procurement
- Procurement to Vendor
- Procurement to Material
- Material to Construction
- Construction to Quality
- Construction to HSE
- Construction to Commissioning
- Commissioning to Handover

### Controls

- Permissions
- Approvals
- Workflows
- Revisions
- Audit Trails
- Status Management

---

# 70. EPC Domain Challenges

The software must account for several challenges.

### 70.1 Large Amount of Data

Large projects can generate huge numbers of documents and transactions.

### 70.2 Complex Relationships

One business object may be related to many other objects.

### 70.3 Parallel Processes

Engineering, procurement, and construction may run simultaneously.

### 70.4 Frequent Changes

Requirements, designs, schedules, and materials may change.

### 70.5 Multiple Stakeholders

Many internal and external users may participate.

### 70.6 Strict Traceability

Project information often needs to be traceable.

### 70.7 Approval Dependencies

Many activities require review and approval.

### 70.8 Project-Specific Requirements

Different clients and projects may have different requirements.

### 70.9 Document Revisions

Documents may go through many revisions.

### 70.10 Schedule and Cost Pressure

Delays and cost overruns can significantly affect project performance.

---

# 71. Why ERP Is Suitable for EPC

ERP systems are useful for EPC organizations because EPC requires integration across departments.

ERP can connect:

**People + Processes + Data + Transactions + Approvals + Reporting**

Instead of:

Engineering using one system

Procurement using another system

Construction using spreadsheets

Quality using separate records

Management using manually prepared reports

an integrated ERP can create a common platform.

---

# 72. Why ERPNext and Frappe Are Suitable

ERPNext already provides many standard enterprise capabilities.

Potential reusable areas include:

- Users
- Roles
- Permissions
- Companies
- Customers
- Suppliers
- Items
- Warehouses
- Purchasing
- Inventory
- Accounting
- Projects
- Employees
- Documents
- Workflows
- Notifications
- Reports

Frappe allows the system to be extended with:

- Custom DocTypes
- Custom fields
- Custom scripts
- Server-side logic
- APIs
- Workflows
- Reports
- Dashboards
- Integrations

Therefore, the project can combine:

**ERPNext Standard Functionality**

with

**EPC-Specific Custom Functionality**

---

# 73. ERPNext Reuse Philosophy

The project should avoid rebuilding functionality that already exists in ERPNext unless there is a strong business reason.

The decision process should be:

**Business Requirement**

→ Does ERPNext support it?

If yes:

**Use / Configure ERPNext**

If partially:

**Extend ERPNext**

If no:

**Build Custom Frappe Functionality**

This approach reduces unnecessary development.

---

# 74. Important Domain Learning for the Developer

Studying EPC helps a software developer understand that enterprise software is not mainly about creating screens and databases.

The developer must understand:

- Business processes
- Real-world workflows
- Roles and responsibilities
- Data ownership
- Approvals
- Dependencies
- Exceptions
- Traceability
- Compliance
- Reporting
- Integration

For example, creating a Purchase Order is technically easy.

Understanding:

**Why the Purchase Order exists → Who requested it → Which project needs it → Which engineering requirement created it → Which vendors were evaluated → Who approved it → When it will arrive → Which inspection is required → Where it will be used**

is the real enterprise software challenge.

---

# 75. Software Developer Learning Outcomes

Studying the EPC domain will help the developer learn:

### Business Analysis

How to convert real business problems into software requirements.

### Domain Modeling

How to identify entities, relationships, states, and processes.

### ERP Design

How enterprise systems integrate multiple departments.

### Workflow Design

How approvals and business states are represented in software.

### Data Modeling

How business entities and transactions relate to each other.

### System Architecture

How different business domains communicate.

### Access Control

How different users receive different permissions.

### Auditability

How business actions are recorded and traced.

### Reporting

How operational data becomes management information.

### Integration

How one business process provides data to another.

---

# 76. Domain-to-Software Translation

The core learning process is:

**Real World**

↓

**Business Concept**

↓

**Business Process**

↓

**Business Entity**

↓

**Business Rule**

↓

**Workflow**

↓

**Data Model**

↓

**ERPNext / Frappe Implementation**

For example:

Real-world concept:

**Vendor quotation**

↓

Business entity:

**Vendor Quotation**

↓

Fields:

- Vendor
- Project
- Items
- Quantity
- Price
- Delivery
- Terms

↓

Business rules:

- Must reference a valid vendor.
- Must contain required items.
- May require technical evaluation.
- May require approval.

↓

Workflow:

Draft  
→ Submitted  
→ Evaluated  
→ Approved / Rejected

↓

Software:

ERPNext / Frappe DocType + Workflow + Permissions + Reports

---

# 77. Domain Study Conclusion

EPC is a complex project-based business domain where Engineering, Procurement, Construction, Quality, HSE, Planning, Cost, Risk, Contracts, Documents, Commissioning, and Handover are interconnected.

The most important characteristic of EPC is not the individual departments.

It is the **relationship between the departments and the flow of information between them**.

The EPC ERP system therefore needs to represent:

**Projects**

+

**Processes**

+

**People**

+

**Materials**

+

**Documents**

+

**Transactions**

+

**Approvals**

+

**Workflows**

+

**Costs**

+

**Schedules**

+

**Quality**

+

**HSE**

+

**Risks**

+

**Changes**

+

**Reporting**

The ultimate objective is to create a single integrated system where project information can move reliably from requirement to execution and finally to handover.

---

# 78. Key Domain Understanding

The most important concepts learned from this study are:

1. EPC means Engineering, Procurement & Construction.
2. EPC is a project-based business model.
3. Engineering creates technical information.
4. Procurement obtains required goods and services.
5. Construction physically executes the project.
6. Engineering, Procurement, and Construction are highly dependent on each other.
7. Quality and HSE operate across project execution.
8. Planning and Cost Control monitor project performance.
9. Risk and Change Management control uncertainty and changes.
10. Document Control manages project information and revisions.
11. Commissioning verifies operational readiness.
12. Handover transfers the completed project to the client or operator.
13. EPC processes frequently run in parallel.
14. Traceability is critical.
15. Workflow and approvals are critical.
16. Master data must be controlled carefully.
17. Transaction data must be connected to projects and master data.
18. ERP systems are suitable because EPC requires cross-department integration.
19. ERPNext should be reused wherever possible.
20. Frappe should be used for EPC-specific extensions.
21. Software design should begin with business understanding.
22. The final ERP system should represent real EPC processes rather than isolated software features.

---

# 79. Next Domain Study Direction

After understanding the general EPC domain, the next stage should study the major EPC business processes in greater detail.

The next analysis should focus on:

**Project Initiation**

→ Contract Management

→ Engineering Management

→ Procurement Management

→ Vendor Management

→ Material Management

→ Construction Management

→ Quality Management

→ HSE Management

→ Planning & Scheduling

→ Cost Control

→ Risk Management

→ Change Management

→ Document Control

→ Commissioning

→ Handover

Each process should later be analyzed using:

- Purpose
- Actors
- Inputs
- Activities
- Outputs
- Business Rules
- Approvals
- Exceptions
- Documents
- Data
- Relationships
- ERPNext Capability
- Custom Frappe Requirements

---

# 80. Current Status

**Document:** `02_Domain_Study_EPC.md`

**Status:** Domain study initiated

**Current Project Phase:** Pre-Development / Documentation & System Design

**Development Status:** Not started

**Primary Objective:** Understand the EPC domain before designing and developing the ERP system.

**Technology Foundation:** ERPNext + Frappe Framework

**Next Step:** Convert the domain understanding into detailed EPC business processes and functional requirements.