# 03 — Business Process Model

**Project:** EPC ERP System  
**Domain:** Engineering, Procurement & Construction (EPC)  
**Platform:** ERPNext + Frappe Framework  
**Document Type:** Business Process Model  
**Document Status:** Draft  
**Version:** 1.0  
**Current Phase:** Pre-Development / Business Process Design

---

## 1. Purpose

This document defines the business processes that the EPC ERP System is expected to represent.

The objective is to move from general EPC domain understanding into a structured model of how work is actually performed inside an EPC organization.

This document focuses on:

- What processes exist
- Why each process exists
- Who participates in each process
- What information enters a process
- What activities occur
- What information is produced
- What approvals are required
- What other processes depend on the output
- What business objects are involved
- Where ERPNext functionality may be reused
- Where custom Frappe functionality may eventually be required

The software should not be designed by simply creating random DocTypes.

The business process should be understood first.

The design principle is:

**Business Process → Activities → Actors → Business Objects → Business Rules → Workflow → Data Model → Software**

---

# 2. What Is a Business Process?

A business process is a structured sequence of activities performed to achieve a specific business outcome.

For example, procurement is not simply a "Purchase Order" screen.

The complete process may be:

**Requirement**

→ Purchase Requisition

→ Request for Quotation

→ Vendor Quotations

→ Technical Evaluation

→ Commercial Evaluation

→ Approval

→ Purchase Order

→ Vendor Execution

→ Inspection

→ Shipment

→ Delivery

→ Receipt

The Purchase Order is only one part of the complete process.

Therefore, the ERP system must model the entire business flow rather than only individual transactions.

---

# 3. EPC Business Process Philosophy

EPC is a project-based business environment.

The major processes are strongly interconnected.

A simplified relationship is:

**Project**

→ Engineering

→ Procurement

→ Material

→ Construction

→ Quality

→ Commissioning

→ Handover

At the same time:

**Planning + Cost + Risk + HSE + Document Control + Change Management**

operate across these processes.

Therefore, the ERP system should be designed as an integrated process platform.

---

# 4. High-Level EPC Business Process Map

The overall EPC process can be represented as:

**Opportunity / Contract**

↓

**Project Initiation**

↓

**Project Planning**

↓

**Engineering**

↓

**Procurement**

↓

**Material & Logistics**

↓

**Construction**

↓

**Quality & Inspection**

↓

**Commissioning**

↓

**Handover**

↓

**Project Closure**

However, these stages are not strictly sequential.

Engineering, Procurement, Construction, Quality, HSE, Planning, and Cost Control may operate simultaneously.

---

# 5. Parallel EPC Execution

A major characteristic of EPC projects is parallel execution.

For example:

**Engineering Area A**

→ Procurement Area A

→ Construction Area A

while at the same time:

**Engineering Area B**

→ Procurement Area B

and:

**Engineering Area C**

is still being designed.

Therefore, the system must support:

- Parallel activities
- Dependencies
- Partial completion
- Multiple project areas
- Multiple disciplines
- Multiple work packages
- Different schedules
- Different responsible teams
- Different statuses

This is an important requirement for the future system architecture.

---

# 6. Main Business Process Groups

The EPC ERP System will organize processes into the following major groups.

### Project and Commercial Processes

1. Opportunity / Contract
2. Project Initiation
3. Project Planning
4. Contract Management

### Engineering Processes

5. Engineering Planning
6. Engineering Deliverables
7. Engineering Review
8. Engineering Approval
9. Engineering Revision Control

### Procurement Processes

10. Material Requirement
11. Purchase Requisition
12. RFQ
13. Vendor Quotation
14. Technical Evaluation
15. Commercial Evaluation
16. Purchase Order
17. Vendor Expediting
18. Inspection
19. Shipment
20. Delivery

### Material Processes

21. Material Receipt
22. Inspection
23. Storage
24. Material Allocation
25. Material Issue
26. Material Consumption

### Construction Processes

27. Construction Planning
28. Work Package Creation
29. Construction Execution
30. Progress Recording
31. Testing
32. Punch List

### Project Control Processes

33. Planning and Scheduling
34. Progress Control
35. Cost Control
36. Risk Management
37. Change Management

### Quality and HSE Processes

38. Quality Planning
39. Inspection and Testing
40. NCR Management
41. Corrective Action
42. HSE Planning
43. HSE Inspection
44. Incident Management
45. HSE Corrective Action

### Information Processes

46. Document Control
47. Revision Management
48. Approval Management
49. Reporting
50. Dashboard Management

### Completion Processes

51. Pre-Commissioning
52. Commissioning
53. Handover
54. Project Closure

---

# 7. Process 1 — Opportunity / Contract

## Purpose

The process establishes the commercial foundation for the EPC project.

## Typical Inputs

- Client requirement
- Tender documents
- Technical specification
- Commercial requirements
- Scope of work
- Contract terms

## Activities

1. Receive opportunity
2. Study client requirements
3. Evaluate technical scope
4. Estimate project requirements
5. Prepare proposal
6. Negotiate
7. Finalize contract
8. Receive contract award

## Outputs

- Contract
- Project scope
- Commercial commitments
- Technical commitments
- Contract milestones

## Main Actors

- Business Development
- Contracts
- Engineering
- Commercial
- Management
- Client

## Important Business Objects

- Client
- Opportunity
- Tender
- Contract
- Contract Milestone

---

# 8. Process 2 — Project Initiation

## Purpose

Project Initiation converts the awarded contract into an executable project.

## Activities

1. Create project
2. Assign project manager
3. Define project organization
4. Define project scope
5. Define project locations
6. Define project phases
7. Define project controls
8. Establish initial schedule
9. Establish communication structure

## Inputs

- Contract
- Scope
- Client requirements

## Outputs

- Project
- Project team
- Project structure
- Initial schedule
- Project baseline information

## Main Actors

- Project Manager
- Management
- Planning
- Contracts
- Finance
- Document Control

---

# 9. Process 3 — Project Planning

## Purpose

Project Planning establishes how the project will be executed.

Planning covers:

- Scope
- Schedule
- Resources
- Cost
- Procurement
- Engineering
- Construction
- Quality
- HSE
- Risk

## Activities

1. Define project breakdown
2. Create WBS
3. Define milestones
4. Create schedule
5. Define responsibilities
6. Establish budget
7. Identify risks
8. Define procurement plan
9. Define engineering plan
10. Define construction plan

## Outputs

- Project execution plan
- WBS
- Schedule
- Budget
- Procurement plan
- Engineering plan
- Construction plan
- Risk register

---

# 10. Process 4 — Contract Management

## Purpose

Contract Management ensures that project execution remains aligned with contractual obligations.

## Activities

- Contract registration
- Contract review
- Obligation tracking
- Milestone tracking
- Contract correspondence
- Variation management
- Claim management
- Contract closure

## Inputs

- Contract
- Client requirements
- Project execution information

## Outputs

- Contract status
- Contract obligations
- Variations
- Claims
- Contract reports

## Main Actors

- Contracts Manager
- Project Manager
- Commercial Team
- Client

---

# 11. Process 5 — Engineering Planning

## Purpose

Engineering Planning determines what engineering work must be completed and when.

## Activities

1. Identify engineering scope
2. Identify disciplines
3. Define deliverables
4. Assign responsible engineers
5. Define planned dates
6. Define review requirements
7. Define approval requirements
8. Track progress

## Outputs

- Engineering deliverable register
- Engineering schedule
- Responsibility assignments

---

# 12. Process 6 — Engineering Deliverables

## Purpose

Engineering Deliverables contain the technical information required for project execution.

Examples:

- Drawings
- Specifications
- Datasheets
- Calculations
- Reports
- Layouts
- Technical documents

## Process

**Engineering Requirement**

↓

**Create Deliverable**

↓

**Internal Review**

↓

**Submit**

↓

**Client Review**

↓

**Approval / Comments**

↓

**Revision if Required**

↓

**Final Approval**

---

# 13. Process 7 — Engineering Review

Engineering documents may require multiple levels of review.

Possible stages:

**Draft**

→ Internal Review

→ Quality Check

→ Project Review

→ Client Review

→ Comments

→ Revision

The exact workflow depends on the project.

---

# 14. Process 8 — Engineering Approval

Approved engineering information becomes the controlled technical basis for downstream activities.

For example:

**Approved Equipment Datasheet**

→ Procurement

**Approved Drawing**

→ Construction

Therefore, engineering approval can act as a gate before procurement or construction.

---

# 15. Process 9 — Engineering Revision Control

Engineering documents may change during project execution.

Example:

Revision 0

→ Revision 1

→ Revision 2

→ Revision 3

The system should preserve:

- Previous revisions
- Current revision
- Revision reason
- Review history
- Approval history
- Effective status

Users should be able to determine which revision was valid at a particular point in time.

---

# 16. Process 10 — Material Requirement

A material requirement identifies what material or equipment is needed for project execution.

Sources may include:

- Engineering
- Construction planning
- Maintenance
- Client requirements
- Project specifications

## Information

- Project
- Material
- Quantity
- Required date
- Required location
- Specification
- Reference document

The requirement can become the starting point for procurement.

---

# 17. Process 11 — Purchase Requisition

A Purchase Requisition formally requests procurement of goods or services.

## Process

**Requirement**

↓

**Purchase Requisition**

↓

**Review**

↓

**Approval**

↓

**Procurement Action**

## Possible Information

- Project
- Requester
- Item
- Quantity
- Required date
- Specification
- Estimated cost
- Priority
- Supporting documents

---

# 18. Process 12 — Request for Quotation

The procurement team identifies suitable vendors and sends RFQs.

## Activities

1. Review requirement
2. Identify vendors
3. Prepare RFQ
4. Send RFQ
5. Receive quotations
6. Register responses

## Outputs

- RFQ
- Vendor responses
- Quotation records

---

# 19. Process 13 — Vendor Quotation

Vendors submit commercial and technical information.

Quotation may contain:

- Vendor
- Items
- Quantity
- Unit price
- Currency
- Delivery time
- Payment terms
- Warranty
- Technical information
- Exceptions

Multiple quotations may be associated with one RFQ.

---

# 20. Process 14 — Technical Evaluation

Engineering or technical specialists evaluate whether vendor proposals satisfy technical requirements.

## Process

**Vendor Quotation**

↓

**Technical Comparison**

↓

**Technical Evaluation**

↓

**Accept / Reject / Clarification**

The evaluation should reference the original technical requirement.

---

# 21. Process 15 — Commercial Evaluation

Commercial evaluation compares:

- Price
- Payment terms
- Delivery
- Warranty
- Taxes
- Freight
- Commercial conditions
- Total cost

Technical and commercial evaluations may be combined to support vendor selection.

---

# 22. Process 16 — Vendor Selection

The organization selects the preferred vendor based on the evaluation process.

Selection may consider:

- Technical compliance
- Price
- Delivery
- Vendor capability
- Quality
- Past performance
- Commercial conditions

Approval may be required before issuing the Purchase Order.

---

# 23. Process 17 — Purchase Order

The Purchase Order formally commits the organization to purchase goods or services from a vendor.

## Process

**Approved Vendor Selection**

↓

**Purchase Order Preparation**

↓

**Internal Approval**

↓

**PO Issued**

↓

**Vendor Acknowledgement**

↓

**Vendor Execution**

The PO becomes an important reference for:

- Procurement
- Finance
- Project Cost
- Vendor
- Logistics
- Quality

---

# 24. Process 18 — Vendor Expediting

Expediting monitors vendor progress after the Purchase Order is issued.

Activities may include:

- Manufacturing status
- Documentation status
- Inspection readiness
- Planned shipment
- Actual shipment
- Delivery forecast

Expediting helps identify delays before they affect construction.

---

# 25. Process 19 — Vendor Inspection

Certain materials or equipment may require inspection before shipment.

Possible process:

**Inspection Requirement**

↓

**Inspection Request**

↓

**Inspection**

↓

**Inspection Result**

↓

**Accepted / Rejected**

↓

**Release for Shipment**

---

# 26. Process 20 — Shipment

Once materials or equipment are ready, shipment is arranged.

Information may include:

- Shipment
- Vendor
- Material
- Quantity
- Transport mode
- Shipping date
- Expected arrival
- Shipping documents

Shipment information should connect to the Purchase Order.

---

# 27. Process 21 — Material Delivery

The material reaches the project site or warehouse.

The system should record:

- Delivery
- Vendor
- Material
- Quantity
- Date
- Location
- Purchase Order
- Shipment reference

---

# 28. Process 22 — Material Receipt

Material Receipt records the organization's acceptance of delivered materials into inventory or project stock.

The receipt should reference:

- Purchase Order
- Vendor
- Material
- Quantity
- Warehouse
- Project
- Delivery information

Receipt may be subject to inspection.

---

# 29. Process 23 — Material Inspection

Received materials may require inspection.

Possible result:

**Accepted**

or

**Rejected**

or

**Accepted with Conditions**

If rejected, the system may initiate:

- NCR
- Return to vendor
- Replacement
- Corrective action

---

# 30. Process 24 — Material Storage

Accepted materials may be stored in:

- Warehouse
- Site storage
- Project yard
- Temporary storage area

The system should maintain visibility of:

- Quantity
- Location
- Status
- Project
- Batch / serial information where applicable

---

# 31. Process 25 — Material Allocation

Materials may be allocated to a particular:

- Project
- Area
- Work Package
- Activity
- Equipment
- Construction scope

Allocation helps prevent uncontrolled material usage.

---

# 32. Process 26 — Material Issue

Materials are issued from storage to construction teams.

Process:

**Material Available**

↓

**Material Request**

↓

**Approval if Required**

↓

**Material Issue**

↓

**Construction Consumption**

---

# 33. Process 27 — Construction Planning

Construction Planning converts project scope into executable work.

Activities include:

- Define construction areas
- Define disciplines
- Create work packages
- Define activities
- Estimate resources
- Identify materials
- Define planned dates
- Define dependencies

---

# 34. Process 28 — Work Package Creation

A Work Package groups related construction activities.

A work package may contain:

- Project
- Area
- Discipline
- Scope
- Activities
- Materials
- Resources
- Planned dates
- Quality requirements
- HSE requirements

---

# 35. Process 29 — Construction Execution

Construction execution represents physical work at the project site.

Examples:

- Excavation
- Foundation
- Structural installation
- Equipment installation
- Piping
- Electrical installation
- Instrumentation
- Testing

Execution depends on:

- Approved engineering information
- Available materials
- Available resources
- Site readiness
- Quality requirements
- HSE requirements

---

# 36. Process 30 — Construction Progress

Progress should be recorded against defined activities or quantities.

Example:

**Planned:** 1,000 meters of cable

**Installed:** 600 meters

**Progress:** 60%

Progress may be recorded:

- Daily
- Weekly
- Monthly

The exact frequency depends on project controls.

---

# 37. Process 31 — Construction Inspection

Construction work may require inspection before being accepted.

Process:

**Construction Activity**

↓

**Inspection Request**

↓

**Inspection**

↓

**Result**

↓

**Accepted / Rejected**

If rejected:

**Corrective Action**

↓

**Reinspection**

---

# 38. Process 32 — Testing

Testing verifies whether installed systems or equipment satisfy requirements.

Examples:

- Pressure test
- Electrical test
- Functional test
- Equipment test
- Instrument test

Testing records should be linked to the relevant project object.

---

# 39. Process 33 — Punch List

A punch item identifies incomplete or defective work.

Examples:

- Missing label
- Minor installation defect
- Missing document
- Incomplete painting
- Testing pending
- Final adjustment required

Process:

**Punch Item Created**

↓

**Assigned**

↓

**Correction**

↓

**Verification**

↓

**Closed**

---

# 40. Process 34 — Quality Planning

Quality Planning establishes how quality will be controlled.

It may define:

- Inspection requirements
- Test requirements
- Acceptance criteria
- Responsible parties
- Required documents
- Inspection points

Quality planning should occur before execution where possible.

---

# 41. Process 35 — Inspection and Test Plan

The Inspection and Test Plan defines inspection and testing requirements.

Typical information:

- Activity
- Inspection type
- Test type
- Acceptance criteria
- Responsible party
- Client witness requirement
- Documentation requirement

---

# 42. Process 36 — NCR Management

NCR means:

**Non-Conformance Report**

NCR process:

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

NCRs may relate to:

- Material
- Engineering
- Construction
- Vendor
- Quality

---

# 43. Process 37 — Corrective Action

Corrective actions address identified problems.

A corrective action should contain:

- Problem
- Root cause
- Action
- Responsible person
- Due date
- Verification
- Closure

Corrective actions may originate from:

- NCR
- HSE incident
- Inspection
- Audit
- Observation

---

# 44. Process 38 — HSE Planning

HSE Planning establishes safety and environmental controls before execution.

It may include:

- Risk assessment
- Safety plans
- Environmental plans
- Site requirements
- Emergency procedures
- Training requirements

---

# 45. Process 39 — HSE Inspection

HSE inspections monitor site conditions.

Process:

**Inspection Planned**

↓

**Inspection Conducted**

↓

**Findings Recorded**

↓

**Corrective Actions**

↓

**Verification**

↓

**Closure**

---

# 46. Process 40 — Incident Management

HSE incident process:

**Incident Occurs**

↓

**Incident Report**

↓

**Investigation**

↓

**Root Cause Analysis**

↓

**Corrective / Preventive Action**

↓

**Verification**

↓

**Closure**

The system should preserve incident history and related actions.

---

# 47. Process 41 — Planning and Scheduling

Planning manages project timelines.

Typical activities:

1. Create activities
2. Define dependencies
3. Assign dates
4. Create baseline
5. Record actual progress
6. Calculate variance
7. Forecast completion

---

# 48. Process 42 — Progress Control

Progress Control compares planned and actual performance.

Example:

**Planned Progress = 70%**

**Actual Progress = 60%**

**Variance = -10%**

The system should allow management to identify delayed areas.

---

# 49. Process 43 — Cost Control

Cost Control monitors project financial performance.

Core concepts:

- Budget
- Planned Cost
- Committed Cost
- Actual Cost
- Forecast Cost
- Variance

Process:

**Budget**

↓

**Commitment**

↓

**Actual Cost**

↓

**Forecast**

↓

**Variance Analysis**

---

# 50. Process 44 — Risk Management

Risk process:

**Risk Identified**

↓

**Risk Assessment**

↓

**Risk Score**

↓

**Risk Owner**

↓

**Mitigation Plan**

↓

**Monitoring**

↓

**Review**

↓

**Close / Accept / Escalate**

Risk should be linked to project activities where appropriate.

---

# 51. Process 45 — Change Management

Changes may affect:

- Scope
- Cost
- Schedule
- Engineering
- Procurement
- Construction

Process:

**Change Identified**

↓

**Change Request**

↓

**Impact Analysis**

↓

**Technical Review**

↓

**Cost Review**

↓

**Schedule Review**

↓

**Approval**

↓

**Implementation**

↓

**Verification**

↓

**Closure**

---

# 52. Process 46 — Document Control

Document Control manages project information.

Process:

**Document Created**

↓

**Registration**

↓

**Review**

↓

**Approval**

↓

**Issue**

↓

**Distribution**

↓

**Revision**

↓

**Re-Review**

Document Control should maintain document history.

---

# 53. Process 47 — Document Revision Management

Document revision process:

**Current Revision**

↓

**Change Required**

↓

**New Revision**

↓

**Review**

↓

**Approval**

↓

**New Revision Becomes Current**

Previous revisions remain available for historical traceability.

---

# 54. Process 48 — Approval Management

Many EPC transactions require approval.

Examples:

- Purchase Requisition
- Purchase Order
- Engineering Document
- Change Request
- NCR Closure
- Handover Package

A generic approval flow can be:

**Draft**

↓

**Submitted**

↓

**Under Review**

↓

**Approved / Rejected**

If rejected:

**Revision**

↓

**Resubmission**

---

# 55. Process 49 — Commissioning

Commissioning verifies that completed systems can operate correctly.

Process:

**Construction Complete**

↓

**Pre-Commissioning**

↓

**Inspection**

↓

**Testing**

↓

**Functional Verification**

↓

**Punch Closure**

↓

**Commissioning Complete**

---

# 56. Process 50 — Handover

Handover transfers the completed project or facility to the client or operational organization.

Handover may require:

- As-built drawings
- Test records
- Inspection records
- Certificates
- Operation manuals
- Maintenance documents
- Quality records
- HSE records
- Punch-list closure

Process:

**Project Completion**

↓

**Handover Preparation**

↓

**Document Compilation**

↓

**Verification**

↓

**Client Review**

↓

**Acceptance**

↓

**Handover**

---

# 57. Process 51 — Project Closure

Project Closure occurs after major project obligations have been completed.

Activities may include:

- Final documentation
- Final accounts
- Contract closure
- Final cost
- Lessons learned
- Asset handover
- Resource release
- Archive

Final output:

**Closed Project**

---

# 58. Cross-Process Relationship

The most important part of the business process model is how processes connect.

Example:

**Engineering**

↓

Approved Equipment Specification

↓

**Procurement**

↓

Purchase Order

↓

**Vendor**

↓

Delivery

↓

**Material Management**

↓

Material Available

↓

**Construction**

↓

Installation

↓

**Quality**

↓

Inspection / Testing

↓

**Commissioning**

↓

Operational Verification

↓

**Handover**

This demonstrates end-to-end process integration.

---

# 59. Engineering → Procurement Relationship

Engineering creates technical requirements.

Procurement uses those requirements to purchase goods and services.

Relationship:

**Engineering Deliverable**

→ Material / Equipment Requirement

→ Purchase Requisition

→ Procurement

Therefore, an engineering change can potentially affect procurement.

---

# 60. Engineering → Construction Relationship

Construction requires approved engineering information.

Relationship:

**Engineering Drawing**

→ Approval

→ Issue for Construction

→ Construction Activity

Construction should ideally use the correct approved revision.

---

# 61. Procurement → Construction Relationship

Construction requires materials and equipment.

Relationship:

**Purchase Order**

→ Vendor

→ Delivery

→ Receipt

→ Material Availability

→ Construction

Procurement delays can therefore affect construction schedules.

---

# 62. Quality → Construction Relationship

Construction activities may require inspection.

Relationship:

**Construction Activity**

→ Inspection

→ Test

→ Acceptance

If work fails:

**NCR**

→ Corrective Action

→ Reinspection

---

# 63. HSE → Construction Relationship

HSE controls safety during construction.

Relationship:

**Construction Activity**

→ HSE Requirement

→ Site Execution

→ Inspection / Observation

→ Corrective Action

---

# 64. Planning → All Processes

Planning coordinates the project schedule.

Planning may monitor:

- Engineering
- Procurement
- Construction
- Quality
- Commissioning
- Handover

Therefore, Planning is a cross-functional process.

---

# 65. Cost Control → All Processes

Cost information can originate from:

- Engineering
- Procurement
- Construction
- Subcontracts
- Logistics
- Finance

Cost Control combines this information to evaluate project financial performance.

---

# 66. Document Control → All Processes

Document Control supports:

- Engineering
- Procurement
- Quality
- HSE
- Construction
- Commissioning
- Handover
- Contracts

Documents are therefore a cross-functional information layer.

---

# 67. Change Management → All Processes

A project change can affect:

- Engineering
- Procurement
- Construction
- Cost
- Schedule
- Quality
- Contract
- Handover

Therefore, Change Management must support impact analysis across multiple processes.

---

# 68. Risk Management → All Processes

Risks may originate from:

- Engineering
- Procurement
- Vendor
- Construction
- Quality
- HSE
- Schedule
- Cost
- Contract

Risk Management therefore acts across the project.

---

# 69. Core EPC Process Chain

The most important end-to-end chain is:

**Client Requirement**

↓

**Contract**

↓

**Project**

↓

**Engineering**

↓

**Technical Requirement**

↓

**Procurement**

↓

**Vendor**

↓

**Purchase Order**

↓

**Delivery**

↓

**Material**

↓

**Construction**

↓

**Inspection**

↓

**Testing**

↓

**Commissioning**

↓

**Handover**

This chain should be considered a primary reference model for the ERP system.

---

# 70. Example End-to-End Business Scenario

Consider a project requiring an industrial pump.

### Step 1 — Engineering Requirement

Engineering determines that the project requires a pump.

### Step 2 — Technical Specification

Engineering creates the pump specification.

### Step 3 — Approval

The specification is reviewed and approved.

### Step 4 — Purchase Requisition

Procurement requirement is created.

### Step 5 — RFQ

RFQ is sent to qualified vendors.

### Step 6 — Vendor Quotations

Vendors submit quotations.

### Step 7 — Technical Evaluation

Engineering evaluates compliance.

### Step 8 — Commercial Evaluation

Procurement evaluates commercial terms.

### Step 9 — Approval

Preferred vendor is approved.

### Step 10 — Purchase Order

PO is issued.

### Step 11 — Vendor Manufacturing

Vendor manufactures the pump.

### Step 12 — Inspection

Pump is inspected.

### Step 13 — Shipment

Pump is shipped.

### Step 14 — Receipt

Pump arrives at the project site.

### Step 15 — Material Inspection

Receipt is verified.

### Step 16 — Construction

Pump is installed.

### Step 17 — Testing

Pump is tested.

### Step 18 — Commissioning

Pump is commissioned.

### Step 19 — Documentation

All relevant records are compiled.

### Step 20 — Handover

Pump becomes part of the completed project handover.

This scenario demonstrates the need for cross-module integration.

---

# 71. Business Process Inputs

Major process inputs may include:

### Commercial Inputs

- Contract
- Client requirements
- Scope
- Milestones

### Engineering Inputs

- Specifications
- Standards
- Design requirements
- Client comments

### Procurement Inputs

- Material requirements
- Approved specifications
- Vendor information

### Construction Inputs

- Approved drawings
- Materials
- Work packages
- Schedule

### Quality Inputs

- Inspection plans
- Specifications
- Acceptance criteria

### HSE Inputs

- Safety requirements
- Risk assessments
- Site requirements

### Commissioning Inputs

- Completed systems
- Test records
- Quality records

---

# 72. Business Process Outputs

Major outputs include:

- Engineering deliverables
- Procurement transactions
- Purchase Orders
- Vendor records
- Material receipts
- Construction progress
- Inspection records
- NCRs
- HSE records
- Schedule updates
- Cost information
- Risk records
- Change records
- Controlled documents
- Commissioning records
- Handover packages

These outputs may become inputs to other processes.

---

# 73. Business Process Actors

Important actors include:

- Client
- Project Manager
- Engineering Manager
- Engineer
- Procurement Manager
- Buyer
- Vendor
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
- Management
- System Administrator

A detailed role model will be created in a later document.

---

# 74. Business Process States

Most EPC processes require lifecycle states.

Examples:

### Generic

**Draft → Submitted → Approved → Completed**

### Engineering

**Draft → Review → Approved → Issued → Superseded**

### Procurement

**Draft → Submitted → Approved → Ordered → Delivered → Closed**

### Quality

**Open → Inspection → Accepted / Rejected → Corrective Action → Closed**

### Risk

**Identified → Assessed → Mitigating → Monitoring → Closed**

### Change

**Draft → Review → Approved → Implemented → Closed**

These states will later be mapped to Frappe workflows.

---

# 75. Business Rules

Business processes must have rules controlling how they operate.

Examples:

- A Purchase Order should reference a valid vendor.
- A Purchase Order should contain valid items.
- An engineering document should have a revision.
- A controlled document should not be issued without required approval.
- A material receipt should reference the relevant Purchase Order where applicable.
- A rejected inspection may require corrective action.
- An NCR should not be closed without required verification.
- A change should be approved before implementation where required.
- A project should not be marked complete until required completion conditions are satisfied.

The detailed business rules will be documented separately.

---

# 76. Exception Processes

Real-world processes do not always follow the happy path.

The system must eventually support exceptions.

Examples:

### Procurement Exception

Vendor does not respond.

**RFQ → No Response → Follow-up → New Vendor**

### Quality Exception

Material fails inspection.

**Receipt → Inspection → Rejected → NCR / Return / Replacement**

### Engineering Exception

Client rejects document.

**Submission → Rejected → Revision → Resubmission**

### Construction Exception

Required material is unavailable.

**Construction Activity → Material Shortage → Delay / Reschedule**

### Schedule Exception

Activity is delayed.

**Planned Activity → Delay → Impact Analysis → Forecast Update**

These exceptions are important for later workflow design.

---

# 77. Process Dependencies

Important dependencies include:

### Engineering Dependency

Procurement may depend on approved technical information.

### Procurement Dependency

Construction may depend on material availability.

### Material Dependency

Construction may depend on inspected and accepted materials.

### Construction Dependency

Commissioning may depend on construction completion.

### Quality Dependency

Handover may depend on quality record completion.

### Document Dependency

Handover may depend on approved project documentation.

### Schedule Dependency

Project completion depends on completion of critical activities.

---

# 78. EPC Process Hierarchy

Business processes can be organized into levels.

### Level 1 — Enterprise Process

**EPC Project Execution**

### Level 2 — Major Process

- Engineering
- Procurement
- Construction
- Quality
- HSE
- Project Controls
- Commissioning
- Handover

### Level 3 — Subprocess

Example:

**Procurement**

→ Purchase Requisition

→ RFQ

→ Quotation

→ Evaluation

→ Purchase Order

### Level 4 — Activity

Example:

**Quotation Evaluation**

→ Compare Price

→ Compare Delivery

→ Check Technical Compliance

→ Prepare Recommendation

### Level 5 — Transaction

Example:

**Vendor Quotation**

This hierarchy will help later when defining DocTypes and workflows.

---

# 79. Process-to-ERP Mapping Concept

Each business process will eventually be mapped to ERPNext or custom Frappe functionality.

The mapping approach will be:

**Business Process**

↓

**Business Object**

↓

**Existing ERPNext Capability?**

↓

If Yes:

**Reuse / Configure**

If Partial:

**Extend**

If No:

**Custom Frappe Development**

This prevents unnecessary custom development.

---

# 80. Example ERP Mapping

### Vendor

Potential ERPNext capability:

**Supplier**

### Material

Potential ERPNext capability:

**Item**

### Purchase Order

Potential ERPNext capability:

**Purchase Order**

### Warehouse

Potential ERPNext capability:

**Warehouse**

### Employee

Potential ERPNext capability:

**Employee**

### Project

Potential ERPNext capability:

**Project**

### EPC Engineering Deliverable

Potential approach:

**Custom Frappe DocType / Extension**

### EPC NCR

Potential approach:

**Custom Frappe DocType / Extension**

### EPC Work Package

Potential approach:

**Custom Frappe DocType / Extension**

The final mapping must be validated against the actual ERPNext version and business requirements.

---

# 81. Process Integration Architecture Concept

At a high level:

**Project**

acts as a central context.

Around it:

**Engineering**

**Procurement**

**Material**

**Construction**

**Quality**

**HSE**

**Planning**

**Cost**

**Risk**

**Change**

**Documents**

**Commissioning**

**Handover**

These processes share information.

The ERP system should avoid unnecessary duplicate data.

---

# 82. Single Source of Truth

A major objective is to establish reliable project information.

For example:

Instead of storing vendor information separately in:

- Procurement spreadsheet
- Project spreadsheet
- Quality spreadsheet
- Finance spreadsheet

the system should maintain a common vendor master where appropriate.

Similarly, project information should be centralized.

The principle is:

**One Business Entity → One Authoritative Record**

where practical.

---

# 83. Traceability Model

The system should support tracing an object backward and forward.

Example:

**Construction Activity**

can trace backward to:

**Work Package**

→ Material

→ Purchase Order

→ Vendor

→ Procurement Requirement

→ Engineering Requirement

And forward to:

**Inspection**

→ Testing

→ Commissioning

→ Handover

This is called end-to-end traceability.

---

# 84. Status Visibility

Every major process should provide status visibility.

Management should be able to answer questions such as:

- How many engineering documents are pending?
- Which Purchase Orders are delayed?
- Which materials have not arrived?
- Which work packages are behind schedule?
- How many NCRs are open?
- Which HSE actions are overdue?
- Which risks are high?
- Which change requests are awaiting approval?
- Which systems are ready for commissioning?
- What is pending for handover?

The ERP system should provide these answers through reports and dashboards.

---

# 85. Process Performance Measurement

Processes should eventually have measurable KPIs.

Examples:

### Engineering

- On-time deliverables
- Approval cycle time
- Overdue documents

### Procurement

- PR-to-PO cycle time
- Vendor response rate
- On-time delivery
- Procurement delay

### Construction

- Planned vs actual progress
- Productivity
- Work package completion

### Quality

- NCR count
- NCR closure time
- Inspection pass rate

### HSE

- Incident count
- Corrective action closure time

### Planning

- Schedule variance
- Forecast variance

### Cost

- Budget variance
- Cost forecast

These KPIs will later be used in dashboard design.

---

# 86. Business Process Data Flow

A simplified data flow is:

**Client Requirement**

↓

**Contract**

↓

**Project**

↓

**Engineering Data**

↓

**Procurement Data**

↓

**Vendor Data**

↓

**Material Data**

↓

**Construction Data**

↓

**Quality Data**

↓

**Commissioning Data**

↓

**Handover Data**

At the same time:

**Schedule Data**

**Cost Data**

**Risk Data**

**HSE Data**

**Change Data**

**Document Data**

interact with these processes.

---

# 87. Process Ownership

Each major process should eventually have a process owner.

Examples:

| Process | Potential Owner |
|---|---|
| Project Management | Project Manager |
| Contract Management | Contracts Manager |
| Engineering | Engineering Manager |
| Procurement | Procurement Manager |
| Vendor Management | Procurement |
| Material Management | Materials / Warehouse |
| Construction | Construction Manager |
| Quality | Quality Manager |
| HSE | HSE Manager |
| Planning | Planning Manager |
| Cost Control | Cost Controller |
| Risk Management | Project Manager / Risk Owner |
| Change Management | Project Manager / Change Manager |
| Document Control | Document Controller |
| Commissioning | Commissioning Manager |
| Handover | Project Manager / Commissioning |

Actual ownership must be validated against the organization's structure.

---

# 88. Process Governance

Business processes should define:

- Who can create
- Who can review
- Who can approve
- Who can modify
- Who can close
- Who can view
- Who owns the process

These requirements will later influence:

- Frappe Roles
- Permissions
- Workflows
- User Permissions
- DocType configuration

---

# 89. Process Automation Opportunities

After the manual processes are understood, automation opportunities can be identified.

Examples:

### Automatic Notification

Purchase Order approval pending.

→ Notify approver.

### Automatic Reminder

Vendor delivery overdue.

→ Notify procurement user.

### Automatic Status

All required documents approved.

→ Update package readiness.

### Automatic Escalation

NCR remains open beyond due date.

→ Escalate to responsible manager.

### Automatic Reporting

Weekly project status.

→ Generate scheduled report.

Automation should only be designed after the underlying business process is understood.

---

# 90. Process Design Principles

The EPC ERP process model will follow these principles.

### Principle 1 — Model the Real Business

Do not design workflows only because they are technically easy.

### Principle 2 — End-to-End Thinking

Understand the complete lifecycle.

### Principle 3 — Integration

Connect related processes.

### Principle 4 — Traceability

Maintain links between related records.

### Principle 5 — Controlled Changes

Important changes should be reviewed and approved.

### Principle 6 — Clear Ownership

Every major process should have responsible users.

### Principle 7 — Exception Handling

The system must eventually support real-world exceptions.

### Principle 8 — Reuse ERPNext

Use existing ERPNext functionality wherever appropriate.

### Principle 9 — Customization Only Where Required

Use Frappe customization for genuine EPC-specific requirements.

### Principle 10 — Documentation First

Document the process before implementing it.

---

# 91. Process Model Example — Complete Procurement Flow

The complete procurement process can be summarized as:

**Engineering / Construction Requirement**

↓

**Material Requirement**

↓

**Purchase Requisition**

↓

**Approval**

↓

**RFQ**

↓

**Vendor Quotation**

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

**Vendor Acknowledgement**

↓

**Manufacturing / Preparation**

↓

**Expediting**

↓

**Inspection**

↓

**Shipment**

↓

**Delivery**

↓

**Material Receipt**

↓

**Material Availability**

↓

**Construction**

This is one of the most important process chains in the EPC ERP.

---

# 92. Process Model Example — Engineering to Construction

Another important flow is:

**Client Requirement**

↓

**Engineering**

↓

**Design**

↓

**Engineering Deliverable**

↓

**Internal Review**

↓

**Client Review**

↓

**Approval**

↓

**Issued for Construction**

↓

**Construction Work Package**

↓

**Construction Activity**

↓

**Inspection**

↓

**Completion**

This demonstrates why document control and revision management are important.

---

# 93. Process Model Example — Quality

Quality process:

**Quality Requirement**

↓

**Inspection Plan**

↓

**Inspection Request**

↓

**Inspection**

↓

**Test**

↓

**Result**

↓

If Accepted:

**Approval**

↓

**Completion**

If Rejected:

**NCR**

↓

**Corrective Action**

↓

**Reinspection**

↓

**Closure**

---

# 94. Process Model Example — HSE

HSE process:

**HSE Requirement**

↓

**Risk Assessment**

↓

**Site Execution**

↓

**Inspection / Observation**

↓

If Issue:

**Incident / Observation**

↓

**Investigation**

↓

**Corrective Action**

↓

**Verification**

↓

**Closure**

---

# 95. Process Model Example — Change

Change process:

**Change Identified**

↓

**Change Request**

↓

**Technical Impact**

↓

**Cost Impact**

↓

**Schedule Impact**

↓

**Contract Impact**

↓

**Approval**

↓

**Implementation**

↓

**Verification**

↓

**Closure**

---

# 96. Process Model Example — Handover

Handover process:

**Construction Completion**

↓

**Testing**

↓

**Commissioning**

↓

**Punch List**

↓

**Punch Closure**

↓

**Document Compilation**

↓

**Quality Verification**

↓

**Client Review**

↓

**Acceptance**

↓

**Handover**

↓

**Project Closure**

---

# 97. Business Process Model Summary

The EPC ERP System is fundamentally a process integration platform.

The main business chain is:

**Contract**

→ **Project**

→ **Engineering**

→ **Procurement**

→ **Material**

→ **Construction**

→ **Quality**

→ **Commissioning**

→ **Handover**

Cross-functional processes operate across this chain:

**Planning**

**Cost**

**Risk**

**HSE**

**Change**

**Document Control**

**Contracts**

These processes must be connected rather than implemented as isolated systems.

---

# 98. Key Process Understanding

The most important conclusions from this document are:

1. EPC is a process-driven business.
2. EPC processes are highly interconnected.
3. Engineering creates information used by procurement and construction.
4. Procurement provides materials and equipment required for construction.
5. Construction consumes engineering information and materials.
6. Quality verifies materials and executed work.
7. HSE controls safety and environmental requirements.
8. Planning coordinates project activities.
9. Cost Control monitors financial performance.
10. Risk Management monitors uncertainty.
11. Change Management controls project changes.
12. Document Control manages controlled information.
13. Commissioning verifies operational readiness.
14. Handover transfers completed project information and assets.
15. Many EPC processes execute in parallel.
16. Workflow and approvals are fundamental.
17. Exceptions must be considered.
18. Traceability is fundamental to enterprise EPC software.
19. Process outputs often become inputs to other processes.
20. ERPNext should be reused wherever suitable.
21. Custom Frappe development should be based on validated gaps.
22. Business processes should be finalized before detailed software implementation.

---

# 99. Relationship With Previous Documents

## Document 00

`00_Business_Requirements_and_Domain_Model.md`

defines the business and domain foundation.

## Document 01

`01_Project_Overview.md`

defines the overall project, objectives, scope, technology, and development approach.

## Document 02

`02_Domain_Study_EPC.md`

explains the EPC domain and its major business areas.

## Document 03

`03_Business_Process_Model.md`

defines how those business areas operate and interact.

The progression is:

**Business Domain**

↓

**Project Definition**

↓

**Domain Understanding**

↓

**Business Process Model**

↓

**Functional Requirements**

↓

**System Architecture**

↓

**Data Model**

↓

**ERPNext Mapping**

↓

**Frappe Design**

↓

**Development**

---

# 100. Current Project State

**Project Phase:** Pre-Development / Documentation & System Design

**Current Stage:** Business Process Modeling

The project is currently focused on understanding and documenting how an EPC organization operates.

Development should not begin with random DocType creation.

The next stage is to convert the business processes into detailed functional requirements.

The planned progression is:

**Business Process Model**

→ Functional Requirements

→ Non-Functional Requirements

→ Detailed Use Cases

→ System Architecture

→ Data Model

→ ERPNext Capability Mapping

→ Custom Frappe Architecture

→ DocType Design

→ Workflow Design

→ Permission Design

→ UI / UX Design

→ Development

---

# 101. Final Objective

The final objective of this business process model is to ensure that the future EPC ERP system reflects real business operations.

The system should allow information to flow from:

**Client Requirement**

through:

**Contract**

→ **Project**

→ **Engineering**

→ **Procurement**

→ **Material**

→ **Construction**

→ **Quality**

→ **Commissioning**

→ **Handover**

while being controlled by:

**Planning**

**Cost**

**Risk**

**HSE**

**Change Management**

**Document Control**

and **Workflow / Approval Management**.

The fundamental philosophy is:

**Understand the Business → Model the Process → Design the System → Build the Software**

**Current Status:** Business Process Modeling

**Next Step:** Define detailed functional requirements for each EPC process.