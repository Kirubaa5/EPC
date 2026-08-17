# 04 — Functional Requirements

**Project:** EPC ERP System  
**Domain:** Engineering, Procurement & Construction (EPC)  
**Platform:** ERPNext + Frappe Framework  
**Document Type:** Functional Requirements Specification (FRS)  
**Document Status:** Draft  
**Version:** 1.0  
**Current Phase:** Pre-Development / Functional Design

---

# 1. Purpose

This document defines the functional requirements for the EPC ERP System.

The purpose of this document is to translate the EPC business processes identified in:

`03_Business_Process_Model.md`

into clear system-level requirements.

It describes:

- What the system must do
- What users must be able to create
- What information users must be able to manage
- What workflows are required
- What approvals are required
- How business processes should interact
- What information must be traceable
- What notifications and validations are required
- What reports and dashboards are required
- Which functionality may be provided by ERPNext
- Which functionality may require custom Frappe development

This document is a functional blueprint for later system architecture and development.

---

# 2. Functional Requirement Philosophy

The system should not be designed as a collection of isolated screens.

Every functional requirement should be connected to a business process.

The design principle is:

**Business Process**

↓

**Business Requirement**

↓

**Functional Requirement**

↓

**System Behavior**

↓

**Data / Workflow / Permission**

↓

**Implementation**

---

# 3. Functional Requirement Definition

A functional requirement describes a capability that the system must provide.

Examples:

- The system shall allow users to create projects.
- The system shall allow users to create engineering deliverables.
- The system shall allow users to submit documents for review.
- The system shall allow authorized users to approve Purchase Orders.
- The system shall track material delivery status.
- The system shall maintain document revision history.
- The system shall generate project progress reports.

Functional requirements describe **what the system does**, not necessarily **how the code will implement it**.

---

# 4. Functional Scope

The EPC ERP System will initially cover the following functional areas:

1. Organization Management
2. User and Role Management
3. Project Management
4. Contract Management
5. Engineering Management
6. Document Control
7. Procurement Management
8. Vendor Management
9. Material Management
10. Inventory / Warehouse Management
11. Construction Management
12. Quality Management
13. HSE Management
14. Planning and Scheduling
15. Progress Management
16. Cost Control
17. Risk Management
18. Change Management
19. Commissioning
20. Handover
21. Notifications
22. Reporting
23. Dashboards
24. Audit and Traceability
25. Integration with ERPNext Core

---

# 5. Functional Requirement Identification

Each requirement will use an identifier.

Format:

`FR-[MODULE]-[NUMBER]`

Examples:

- FR-PROJ-001
- FR-ENG-001
- FR-PROC-001
- FR-QA-001
- FR-HSE-001

This makes requirements easier to reference during:

- Architecture
- Development
- Testing
- Bug tracking
- GitHub documentation
- Future change management

---

# 6. Requirement Priority

Requirements will be classified using:

### Must Have

Essential for the system to function.

### Should Have

Important functionality that significantly improves the system.

### Could Have

Useful functionality that can be implemented later.

### Future

Potential functionality outside the initial release.

Priority will help define MVP scope.

---

# 7. System Users

The system must support different categories of users.

Potential users include:

- System Administrator
- Project Manager
- Project Engineer
- Engineering Manager
- Engineer
- Procurement Manager
- Procurement User
- Buyer
- Vendor Management User
- Warehouse User
- Construction Manager
- Site Engineer
- Quality Manager
- Quality Engineer
- HSE Manager
- HSE Officer
- Planner
- Cost Controller
- Contract Manager
- Document Controller
- Commissioning Engineer
- Finance User
- Management
- Client User where required

The detailed role and permission model will be defined separately.

---

# 8. FR — Organization Management

## FR-ORG-001 — Company Management

The system shall allow authorized users to create and manage companies.

The company record should support:

- Company name
- Company code
- Address
- Contact information
- Currency
- Tax information
- Status

---

## FR-ORG-002 — Department Management

The system shall allow authorized users to define departments.

Examples:

- Engineering
- Procurement
- Construction
- Quality
- HSE
- Planning
- Finance
- Contracts

---

## FR-ORG-003 — Organization Structure

The system should support organizational relationships.

Example:

**Company**

→ Department

→ Team

→ User

This structure may be integrated with ERPNext's existing organizational capabilities.

---

# 9. FR — User and Role Management

## FR-USER-001 — User Creation

The system shall allow administrators to create users.

User information may include:

- Name
- Email
- Employee
- Department
- Role
- Active / inactive status

---

## FR-USER-002 — Role Assignment

The system shall allow authorized administrators to assign roles.

Examples:

- Project Manager
- Engineer
- Procurement User
- Quality User
- HSE User
- Planner
- Document Controller

---

## FR-USER-003 — Role-Based Access

The system shall restrict functionality based on user permissions.

For example:

An Engineer may create engineering documents.

A Document Controller may control document issuance.

A Project Manager may approve selected project activities.

---

## FR-USER-004 — Project-Based Access

The system should support access restrictions based on project assignment.

A user assigned to Project A should not automatically gain unrestricted access to Project B.

---

# 10. FR — Project Management

## FR-PROJ-001 — Project Creation

The system shall allow authorized users to create EPC projects.

Project information shall include:

- Project name
- Project code
- Client
- Contract
- Location
- Project Manager
- Start date
- Planned completion date
- Status
- Description

---

## FR-PROJ-002 — Project Status

The system shall support project lifecycle statuses.

Example:

**Planned**

→ Active

→ On Hold

→ Completed

→ Closed

---

## FR-PROJ-003 — Project Team

The system shall allow users to assign project team members.

Each team member may have:

- Employee
- Role
- Department
- Responsibility
- Assignment period

---

## FR-PROJ-004 — Project Structure

The system shall support project breakdown.

Example:

**Project**

→ Area

→ Discipline

→ Work Package

→ Activity

---

## FR-PROJ-005 — Project Milestones

The system shall allow users to define project milestones.

Milestones may include:

- Engineering Complete
- Procurement Complete
- Mechanical Completion
- Commissioning
- Handover

---

## FR-PROJ-006 — Project Dashboard

The system should provide a project dashboard containing:

- Overall progress
- Schedule status
- Cost status
- Procurement status
- Engineering status
- Construction status
- Quality status
- HSE status
- Risk status
- Change status

---

# 11. FR — Contract Management

## FR-CON-001 — Contract Creation

The system shall allow authorized users to register contracts.

Contract information may include:

- Contract number
- Client
- Project
- Contract value
- Currency
- Start date
- End date
- Scope
- Terms
- Status

---

## FR-CON-002 — Contract Milestones

The system shall allow users to define contract milestones.

---

## FR-CON-003 — Contract Obligations

The system should allow users to record important contractual obligations.

---

## FR-CON-004 — Contract Changes

The system shall support recording approved contract changes where required.

---

## FR-CON-005 — Contract Status

The system shall support:

- Draft
- Active
- Suspended
- Completed
- Closed

---

# 12. FR — Engineering Management

## FR-ENG-001 — Engineering Deliverable Creation

The system shall allow authorized engineering users to create engineering deliverables.

Examples:

- Drawing
- Specification
- Datasheet
- Calculation
- Report
- Layout

---

## FR-ENG-002 — Engineering Deliverable Register

The system shall maintain a central register of engineering deliverables.

The register should include:

- Document number
- Title
- Discipline
- Project
- Responsible person
- Revision
- Status
- Planned date
- Actual date

---

## FR-ENG-003 — Engineering Discipline

The system shall allow deliverables to be associated with a discipline.

Examples:

- Civil
- Structural
- Mechanical
- Electrical
- Instrumentation
- Process
- Piping

---

## FR-ENG-004 — Engineering Revision

The system shall maintain revision information for engineering deliverables.

---

## FR-ENG-005 — Engineering Review

The system shall allow authorized users to submit engineering documents for review.

---

## FR-ENG-006 — Engineering Approval

The system shall support approval of engineering documents.

---

## FR-ENG-007 — Engineering Rejection

The system shall allow reviewers to reject documents with comments.

---

## FR-ENG-008 — Engineering Resubmission

The system shall allow rejected documents to be revised and resubmitted.

---

## FR-ENG-009 — Engineering Document Status

The system should support statuses such as:

- Draft
- Internal Review
- Submitted
- Client Review
- Approved
- Rejected
- Issued
- Superseded

---

## FR-ENG-010 — Engineering Traceability

The system shall allow engineering documents to be linked to:

- Project
- Work Package
- Material
- Procurement Requirement
- Construction Activity

---

# 13. FR — Document Control

## FR-DOC-001 — Document Registration

The system shall allow authorized users to register project documents.

---

## FR-DOC-002 — Document Numbering

The system should support controlled document numbering.

---

## FR-DOC-003 — Document Revision

The system shall maintain document revision history.

---

## FR-DOC-004 — Document Review

The system shall support document review workflows.

---

## FR-DOC-005 — Document Approval

The system shall support controlled document approval.

---

## FR-DOC-006 — Document Issue

Authorized users shall be able to issue approved documents.

---

## FR-DOC-007 — Superseded Documents

The system shall identify previous revisions as superseded when a new approved revision becomes effective.

---

## FR-DOC-008 — Document Search

Users shall be able to search documents using:

- Document number
- Title
- Project
- Discipline
- Revision
- Status
- Date

---

## FR-DOC-009 — Document Attachments

The system shall allow appropriate files to be attached to document records.

---

## FR-DOC-010 — Document History

The system shall preserve document lifecycle history.

---

# 14. FR — Procurement Management

## FR-PROC-001 — Material Requirement

The system shall allow authorized users to create material requirements.

---

## FR-PROC-002 — Purchase Requisition

The system shall allow users to create Purchase Requisitions.

The requisition should contain:

- Project
- Requester
- Item
- Quantity
- Required date
- Specification
- Priority

---

## FR-PROC-003 — Purchase Requisition Approval

The system shall support approval workflows for Purchase Requisitions.

---

## FR-PROC-004 — RFQ Creation

The system shall allow procurement users to create RFQs.

---

## FR-PROC-005 — Vendor Selection for RFQ

The system shall allow users to select one or more vendors for an RFQ.

---

## FR-PROC-006 — Vendor Quotation

The system shall allow vendor quotations to be recorded.

---

## FR-PROC-007 — Technical Evaluation

The system shall allow technical users to evaluate vendor quotations.

---

## FR-PROC-008 — Commercial Evaluation

The system shall allow commercial users to evaluate vendor quotations.

---

## FR-PROC-009 — Vendor Comparison

The system should provide comparison functionality for multiple vendor quotations.

---

## FR-PROC-010 — Vendor Selection

The system shall allow authorized users to select the preferred vendor.

---

## FR-PROC-011 — Purchase Order

The system shall allow users to create Purchase Orders.

---

## FR-PROC-012 — Purchase Order Approval

The system shall support Purchase Order approval workflows.

---

## FR-PROC-013 — Purchase Order Status

The system shall track Purchase Order status.

Example:

**Draft**

→ Submitted

→ Approved

→ Issued

→ Acknowledged

→ Partially Delivered

→ Fully Delivered

→ Closed

---

## FR-PROC-014 — Vendor Delivery Tracking

The system shall allow users to track expected and actual delivery dates.

---

## FR-PROC-015 — Expediting

The system should allow procurement users to record vendor progress and expediting information.

---

## FR-PROC-016 — Procurement Traceability

The system shall allow users to trace:

**Requirement**

→ PR

→ RFQ

→ Quotation

→ Evaluation

→ PO

→ Delivery

→ Receipt

---

# 15. FR — Vendor Management

## FR-VEND-001 — Vendor Registration

The system shall allow authorized users to create vendor records.

---

## FR-VEND-002 — Vendor Profile

Vendor profiles may include:

- Name
- Address
- Contact
- Category
- Qualification
- Status
- Performance information

---

## FR-VEND-003 — Vendor Qualification

The system should support vendor qualification information.

---

## FR-VEND-004 — Vendor Performance

The system should allow vendor performance to be evaluated.

Possible factors:

- Quality
- Delivery
- Cost
- Responsiveness
- Compliance

---

## FR-VEND-005 — Vendor Status

The system should support:

- Pending
- Approved
- Blocked
- Inactive

---

# 16. FR — Material Management

## FR-MAT-001 — Material Master

The system shall maintain material / item information.

---

## FR-MAT-002 — Material Requirement

The system shall link materials to project requirements.

---

## FR-MAT-003 — Material Availability

The system should allow users to determine whether required materials are available.

---

## FR-MAT-004 — Material Allocation

The system shall allow materials to be allocated to projects, areas, or work packages.

---

## FR-MAT-005 — Material Issue

The system shall allow authorized users to issue materials.

---

## FR-MAT-006 — Material Consumption

The system should track material consumption against project activities.

---

# 17. FR — Inventory and Warehouse

## FR-WH-001 — Warehouse Management

The system shall support project warehouses and storage locations.

---

## FR-WH-002 — Material Receipt

The system shall allow materials to be received against applicable purchase transactions.

---

## FR-WH-003 — Stock Visibility

Users shall be able to view available material quantities.

---

## FR-WH-004 — Material Location

The system shall identify where material is stored.

---

## FR-WH-005 — Material Transfer

The system should support transferring materials between appropriate storage locations.

---

## FR-WH-006 — Material Status

Material may have statuses such as:

- Expected
- Received
- Under Inspection
- Accepted
- Rejected
- Available
- Allocated
- Issued

---

# 18. FR — Construction Management

## FR-CONST-001 — Construction Area

The system shall allow projects to be divided into construction areas.

---

## FR-CONST-002 — Work Package

The system shall allow users to create construction work packages.

---

## FR-CONST-003 — Construction Activity

The system shall allow users to define construction activities.

---

## FR-CONST-004 — Activity Assignment

Activities shall be assignable to responsible teams or users.

---

## FR-CONST-005 — Construction Schedule

The system shall allow construction activities to have planned dates.

---

## FR-CONST-006 — Construction Progress

The system shall allow actual progress to be recorded.

---

## FR-CONST-007 — Quantity-Based Progress

The system should support progress based on measurable quantities.

Example:

**Planned Quantity:** 1,000 meters

**Completed:** 600 meters

**Progress:** 60%

---

## FR-CONST-008 — Construction Dependencies

The system should support dependencies between construction activities.

---

## FR-CONST-009 — Construction Completion

The system shall allow activities to be marked complete after required conditions are satisfied.

---

# 19. FR — Quality Management

## FR-QA-001 — Quality Plan

The system shall allow quality plans to be created for projects.

---

## FR-QA-002 — Inspection and Test Plan

The system shall allow users to create Inspection and Test Plans.

---

## FR-QA-003 — Inspection Request

The system shall allow users to create inspection requests.

---

## FR-QA-004 — Inspection Result

The system shall allow inspection results to be recorded.

Possible results:

- Accepted
- Rejected
- Accepted with Comments

---

## FR-QA-005 — Test Record

The system shall allow testing information to be recorded.

---

## FR-QA-006 — NCR Creation

The system shall allow users to create Non-Conformance Reports.

---

## FR-QA-007 — NCR Investigation

The system shall allow users to record investigation details.

---

## FR-QA-008 — Corrective Action

The system shall allow corrective actions to be assigned.

---

## FR-QA-009 — NCR Closure

The system shall only allow NCR closure after required verification.

---

## FR-QA-010 — Quality Traceability

Quality records shall be linkable to relevant:

- Project
- Material
- Vendor
- Construction Activity
- Engineering Document

---

# 20. FR — HSE Management

## FR-HSE-001 — Risk Assessment

The system shall allow HSE risk assessments to be recorded.

---

## FR-HSE-002 — HSE Inspection

The system shall allow HSE inspections to be created and recorded.

---

## FR-HSE-003 — HSE Observation

Users shall be able to record safety observations.

---

## FR-HSE-004 — Incident Management

The system shall allow HSE incidents to be recorded.

---

## FR-HSE-005 — Incident Investigation

The system shall allow investigation information to be recorded.

---

## FR-HSE-006 — HSE Corrective Action

The system shall allow corrective actions to be assigned and tracked.

---

## FR-HSE-007 — HSE Closure

The system shall track corrective actions until closure.

---

# 21. FR — Planning and Scheduling

## FR-PLAN-001 — Project Schedule

The system shall allow project activities to be planned.

---

## FR-PLAN-002 — Activity Dependencies

The system should support activity dependencies.

---

## FR-PLAN-003 — Baseline Schedule

The system should allow approved schedules to be baselined.

---

## FR-PLAN-004 — Actual Progress

The system shall allow actual progress to be recorded.

---

## FR-PLAN-005 — Schedule Variance

The system shall calculate or report planned versus actual performance.

---

## FR-PLAN-006 — Forecast

The system should support forecast completion dates.

---

# 22. FR — Progress Management

## FR-PROG-001 — Progress Recording

The system shall allow project progress to be recorded.

---

## FR-PROG-002 — Progress by Area

Progress should be viewable by project area.

---

## FR-PROG-003 — Progress by Discipline

Progress should be viewable by discipline.

---

## FR-PROG-004 — Progress by Work Package

Progress should be viewable by work package.

---

## FR-PROG-005 — Planned vs Actual

The system shall provide planned versus actual progress.

---

## FR-PROG-006 — Progress Reporting

The system shall generate progress reports.

---

# 23. FR — Cost Control

## FR-COST-001 — Project Budget

The system shall allow project budgets to be defined.

---

## FR-COST-002 — Cost Commitment

The system should track committed project costs.

---

## FR-COST-003 — Actual Cost

The system should capture actual project costs from relevant transactions.

---

## FR-COST-004 — Forecast Cost

The system should support forecast cost.

---

## FR-COST-005 — Cost Variance

The system should calculate or report:

**Budget vs Actual**

and:

**Budget vs Forecast**

---

## FR-COST-006 — Cost by Project

Users shall be able to view costs by project.

---

## FR-COST-007 — Cost by Work Package

The system should support cost visibility at work package level where required.

---

# 24. FR — Risk Management

## FR-RISK-001 — Risk Register

The system shall maintain a project risk register.

---

## FR-RISK-002 — Risk Identification

Users shall be able to create risks.

---

## FR-RISK-003 — Risk Assessment

Users shall be able to evaluate risks using defined criteria.

---

## FR-RISK-004 — Risk Owner

Each active risk should have an assigned owner.

---

## FR-RISK-005 — Mitigation Plan

The system shall allow mitigation actions to be recorded.

---

## FR-RISK-006 — Risk Monitoring

The system shall track risk status.

---

## FR-RISK-007 — Risk Escalation

The system should support escalation of significant risks.

---

# 25. FR — Change Management

## FR-CHG-001 — Change Request

The system shall allow users to create change requests.

---

## FR-CHG-002 — Change Description

A change request shall contain the proposed change and reason.

---

## FR-CHG-003 — Impact Analysis

The system shall support analysis of:

- Technical impact
- Cost impact
- Schedule impact
- Contract impact
- Procurement impact
- Construction impact

---

## FR-CHG-004 — Change Approval

The system shall support change approval workflows.

---

## FR-CHG-005 — Change Implementation

Approved changes shall be tracked through implementation.

---

## FR-CHG-006 — Change Closure

The system shall allow changes to be closed after implementation and verification.

---

# 26. FR — Commissioning

## FR-COM-001 — Commissioning Plan

The system shall allow commissioning plans to be created.

---

## FR-COM-002 — System / Subsystem

The system should support project systems and subsystems.

---

## FR-COM-003 — Pre-Commissioning

The system shall allow pre-commissioning activities to be tracked.

---

## FR-COM-004 — Commissioning Test

The system shall allow commissioning tests to be recorded.

---

## FR-COM-005 — Commissioning Status

The system shall provide commissioning status visibility.

---

## FR-COM-006 — Commissioning Punch List

The system should allow commissioning punch items to be tracked.

---

# 27. FR — Handover Management

## FR-HAND-001 — Handover Package

The system shall allow handover packages to be created.

---

## FR-HAND-002 — Handover Documents

The system shall identify required handover documents.

---

## FR-HAND-003 — Document Completeness

The system should check whether required documents are available before handover.

---

## FR-HAND-004 — Punch Closure

The system should verify required punch items are closed before final handover where applicable.

---

## FR-HAND-005 — Client Acceptance

The system shall record client acceptance where applicable.

---

## FR-HAND-006 — Handover Status

The system shall track:

- Preparation
- Internal Review
- Client Review
- Accepted
- Completed

---

# 28. FR — Project Closure

## FR-CLOSE-001 — Closure Checklist

The system should provide a project closure checklist.

---

## FR-CLOSE-002 — Final Documentation

The system shall allow final project documentation to be identified.

---

## FR-CLOSE-003 — Final Cost

The system should provide final project cost information.

---

## FR-CLOSE-004 — Lessons Learned

The system should allow lessons learned to be recorded.

---

## FR-CLOSE-005 — Project Closure

Authorized users shall be able to close the project after required conditions are satisfied.

---

# 29. FR — Notification Management

## FR-NOTIF-001 — Workflow Notifications

The system shall notify users when an action requires their attention.

---

## FR-NOTIF-002 — Approval Notification

Approvers should receive notifications when records are awaiting approval.

---

## FR-NOTIF-003 — Overdue Notification

The system should notify responsible users when important tasks become overdue.

---

## FR-NOTIF-004 — Escalation

The system should support escalation for overdue critical actions.

---

## FR-NOTIF-005 — Status Notification

Important status changes should generate notifications where appropriate.

---

# 30. FR — Reporting

## FR-REP-001 — Project Status Report

The system shall provide project status reporting.

---

## FR-REP-002 — Engineering Report

The system should provide engineering deliverable status reports.

---

## FR-REP-003 — Procurement Report

The system shall provide procurement status reports.

---

## FR-REP-004 — Material Report

The system should provide material availability and delivery reports.

---

## FR-REP-005 — Construction Report

The system shall provide construction progress reports.

---

## FR-REP-006 — Quality Report

The system should provide:

- Inspection status
- NCR status
- Corrective action status

---

## FR-REP-007 — HSE Report

The system should provide:

- Incident status
- Observation status
- Corrective action status

---

## FR-REP-008 — Schedule Report

The system shall provide schedule performance information.

---

## FR-REP-009 — Cost Report

The system should provide project cost information.

---

## FR-REP-010 — Risk Report

The system shall provide project risk information.

---

## FR-REP-011 — Change Report

The system should provide change request status.

---

## FR-REP-012 — Handover Report

The system should provide handover readiness information.

---

# 31. FR — Dashboards

## FR-DASH-001 — Management Dashboard

The system should provide high-level project information.

Possible KPIs:

- Overall Progress
- Schedule Variance
- Cost Variance
- Open Risks
- Open NCRs
- HSE Incidents
- Procurement Delays
- Engineering Delays
- Handover Readiness

---

## FR-DASH-002 — Project Dashboard

The Project Manager should have access to project-specific information.

---

## FR-DASH-003 — Engineering Dashboard

Engineering users should see:

- Deliverables
- Pending reviews
- Overdue documents
- Approval status
- Revision status

---

## FR-DASH-004 — Procurement Dashboard

Procurement users should see:

- Open PRs
- RFQs
- Pending quotations
- Open POs
- Delayed deliveries
- Vendor performance

---

## FR-DASH-005 — Construction Dashboard

Construction users should see:

- Work packages
- Activities
- Progress
- Delays
- Material availability
- Open inspections

---

## FR-DASH-006 — Quality Dashboard

Quality users should see:

- Inspections
- Pass/fail status
- NCRs
- Corrective actions

---

## FR-DASH-007 — HSE Dashboard

HSE users should see:

- Incidents
- Observations
- Open actions
- Risk status

---

# 32. FR — Search

## FR-SEARCH-001 — Global Search

The system should allow users to search relevant project information.

---

## FR-SEARCH-002 — Project Search

Users should be able to search by:

- Project code
- Project name
- Client

---

## FR-SEARCH-003 — Document Search

Users should be able to search by:

- Document number
- Revision
- Title
- Discipline
- Project

---

## FR-SEARCH-004 — Procurement Search

Users should be able to search:

- PR
- RFQ
- Quotation
- PO
- Vendor

---

# 33. FR — Audit and Traceability

## FR-AUDIT-001 — Record History

The system shall preserve important record history.

---

## FR-AUDIT-002 — Status History

The system should preserve status transitions.

---

## FR-AUDIT-003 — Approval History

The system shall preserve approval information.

---

## FR-AUDIT-004 — Revision History

The system shall preserve document and engineering revisions.

---

## FR-AUDIT-005 — User Tracking

Important actions should be associated with the user who performed them.

---

## FR-AUDIT-006 — Timestamp

Important transactions should retain creation and modification timestamps.

---

# 34. FR — Workflow

## FR-WF-001 — Workflow Configuration

The system shall support configurable workflows for important business processes.

---

## FR-WF-002 — Approval Levels

The system should support multiple approval levels where required.

Example:

**Engineer**

→ Engineering Manager

→ Project Manager

→ Client

---

## FR-WF-003 — Rejection

A reviewer shall be able to reject a transaction with a reason.

---

## FR-WF-004 — Resubmission

Rejected records should be resubmittable after correction.

---

## FR-WF-005 — Workflow History

The system shall preserve workflow transition history.

---

# 35. FR — Validation

## FR-VAL-001 — Required Fields

The system shall prevent submission of records missing mandatory information.

---

## FR-VAL-002 — Date Validation

The system shall validate relevant dates.

Example:

Completion date should not incorrectly precede the start date.

---

## FR-VAL-003 — Quantity Validation

The system shall validate quantities where required.

---

## FR-VAL-004 — Status Validation

The system shall prevent invalid status transitions.

---

## FR-VAL-005 — Reference Validation

The system shall ensure required referenced records exist.

---

## FR-VAL-006 — Duplicate Prevention

The system should prevent duplicate records where unique business identifiers are required.

---

# 36. FR — Attachment Management

## FR-ATT-001 — File Attachment

Users shall be able to attach supporting files to relevant records.

---

## FR-ATT-002 — Supporting Documents

Records such as:

- PR
- RFQ
- PO
- Engineering Document
- Inspection
- NCR
- Change Request

should support relevant attachments.

---

## FR-ATT-003 — Document Security

Access to attachments shall follow appropriate permissions.

---

# 37. FR — ERPNext Integration

The system should reuse ERPNext standard capabilities wherever suitable.

Potential standard ERPNext capabilities include:

- Company
- Customer
- Supplier
- Item
- Warehouse
- Purchase Requisition / Material Request
- Request for Quotation
- Supplier Quotation
- Purchase Order
- Purchase Receipt
- Stock Entry
- Project
- Task
- Employee
- User
- Role
- Accounting
- Workflow
- File
- Communication
- Notification
- Reports

The exact mapping will be validated during the ERPNext Capability Mapping phase.

---

# 38. FR — Custom Frappe Functionality

Potential EPC-specific custom functionality may include:

- Engineering Deliverable
- Engineering Revision
- Engineering Review
- Work Package
- Construction Activity
- Inspection Request
- NCR
- HSE Incident
- Risk Register
- Change Request
- Commissioning Record
- Handover Package
- EPC-specific dashboards
- EPC-specific project controls

These should only be custom-developed if existing ERPNext functionality cannot appropriately satisfy the requirement.

---

# 39. Functional Integration Requirements

The system shall support integration between major modules.

### Engineering → Procurement

Approved technical requirements should be available to procurement.

### Procurement → Material

Purchase and delivery information should update material availability.

### Material → Construction

Construction should know whether required materials are available.

### Construction → Quality

Construction activities should trigger required inspections.

### Quality → Commissioning

Completed inspections and tests should support commissioning readiness.

### Commissioning → Handover

Commissioning records should contribute to handover packages.

### All Processes → Project Controls

Relevant transactions should contribute to progress, cost, schedule, risk, and reporting.

---

# 40. End-to-End Traceability Requirement

The system should support a traceability chain such as:

**Project**

↓

**Engineering Requirement**

↓

**Engineering Deliverable**

↓

**Material Requirement**

↓

**Purchase Requisition**

↓

**RFQ**

↓

**Vendor Quotation**

↓

**Purchase Order**

↓

**Delivery**

↓

**Material Receipt**

↓

**Construction Activity**

↓

**Inspection**

↓

**Testing**

↓

**Commissioning**

↓

**Handover**

Users should be able to navigate between related records.

---

# 41. Functional Requirements for EPC Lifecycle

The minimum complete lifecycle should support:

**1. Contract**

↓

**2. Project**

↓

**3. Planning**

↓

**4. Engineering**

↓

**5. Procurement**

↓

**6. Material**

↓

**7. Construction**

↓

**8. Quality**

↓

**9. HSE**

↓

**10. Commissioning**

↓

**11. Handover**

↓

**12. Closure**

Cross-functional processes:

**Cost**

**Schedule**

**Risk**

**Change**

**Document Control**

must operate throughout the lifecycle.

---

# 42. MVP Functional Scope

The first implementation should focus on the most important capabilities.

## MVP — Phase 1

### Project

- Project creation
- Project structure
- Project team
- Project status

### Engineering

- Engineering deliverable
- Revision
- Review
- Approval
- Document status

### Procurement

- Material requirement
- Purchase Requisition
- RFQ
- Vendor Quotation
- Evaluation
- Purchase Order

### Material

- Material receipt
- Material status
- Material allocation
- Material issue

### Construction

- Work package
- Construction activity
- Progress

### Quality

- Inspection
- NCR
- Corrective action

### HSE

- Risk assessment
- Incident
- Corrective action

### Project Controls

- Schedule
- Progress
- Cost
- Risk

### Documents

- Document register
- Revision
- Approval
- Attachments

---

# 43. Phase 2 Functional Scope

Potential Phase 2 features:

- Advanced procurement tracking
- Vendor performance
- Expediting
- Advanced construction planning
- Advanced quality management
- Advanced HSE
- Advanced cost control
- Change management
- Commissioning
- Handover management
- Advanced dashboards

---

# 44. Future Functional Scope

Potential future features:

- Mobile site application
- Advanced analytics
- Predictive project analytics
- AI-assisted document classification
- AI-based schedule risk prediction
- Automated vendor performance analysis
- Advanced forecasting
- IoT integration
- BIM integration
- External client portal
- Advanced workflow automation

These features are not part of the initial development scope unless explicitly approved.

---

# 45. Functional Requirement Prioritization

| Area | Priority |
|---|---|
| Project Management | Must Have |
| Engineering | Must Have |
| Procurement | Must Have |
| Material Management | Must Have |
| Construction | Must Have |
| Quality | Must Have |
| HSE | Must Have |
| Planning | Must Have |
| Document Control | Must Have |
| Cost Control | Must Have |
| Risk Management | Should Have |
| Change Management | Should Have |
| Commissioning | Should Have |
| Handover | Should Have |
| Advanced Analytics | Future |
| AI Features | Future |
| BIM Integration | Future |

This priority is preliminary and must be validated before implementation.

---

# 46. Functional Requirement Traceability

Each functional requirement should eventually be traceable to:

**Business Requirement**

→ **Business Process**

→ **Functional Requirement**

→ **Use Case**

→ **DocType / Data Model**

→ **Workflow**

→ **Permission**

→ **Implementation**

→ **Test Case**

Example:

**Business Process:** Procurement

↓

**Requirement:** Purchase orders require approval

↓

**FR-PROC-012**

↓

**Use Case:** Approve Purchase Order

↓

**DocType:** Purchase Order

↓

**Workflow:** Draft → Pending Approval → Approved

↓

**Role:** Procurement Manager

↓

**Implementation:** ERPNext Workflow / Frappe

↓

**Test:** Verify unauthorized user cannot approve

---

# 47. Functional Requirement Acceptance

A functional requirement should eventually have measurable acceptance criteria.

Example:

### Requirement

`FR-PROC-012 — Purchase Order Approval`

### Acceptance Criteria

1. User can submit a Purchase Order.
2. Purchase Order enters approval state.
3. Authorized approver receives notification.
4. Unauthorized user cannot approve.
5. Approver can approve.
6. Approver can reject.
7. Rejection requires a reason where configured.
8. Approval history is recorded.
9. Approved Purchase Order cannot be modified without appropriate permission.
10. Status is visible in reports.

This approach will later make testing easier.

---

# 48. Functional Requirements and Frappe

Frappe provides several capabilities that can support these requirements.

Potential Frappe capabilities include:

- DocTypes
- Child Tables
- Workflows
- Roles
- Role Permissions
- User Permissions
- Doc Events
- Server Scripts where appropriate
- Client Scripts
- Reports
- Query Reports
- Script Reports
- Dashboards
- Notifications
- Email Alerts
- Attachments
- Background Jobs
- REST APIs
- Custom Pages
- Web Forms
- Print Formats

The final technical design should select the simplest appropriate mechanism.

---

# 49. Functional Requirements and ERPNext

ERPNext already provides many enterprise processes.

Therefore, the system should follow this strategy:

**Reuse**

→ standard ERPNext functionality where possible.

**Configure**

→ adapt existing functionality through configuration.

**Extend**

→ add fields, workflows, reports, and controlled customizations.

**Customize**

→ create custom Frappe functionality for EPC-specific processes.

The goal is not to rebuild ERPNext.

The goal is to build an EPC solution on top of ERPNext and Frappe.

---

# 50. Functional Design Principles

The following principles apply to all functional requirements:

1. Business-first design.
2. Reuse ERPNext wherever possible.
3. Avoid unnecessary customization.
4. Maintain traceability.
5. Use controlled workflows.
6. Enforce business rules.
7. Provide role-based access.
8. Maintain audit history.
9. Support parallel project execution.
10. Support exceptions.
11. Keep data centralized.
12. Avoid unnecessary duplicate records.
13. Design for reporting from the beginning.
14. Design for future scalability.
15. Keep requirements testable.

---

# 51. Key Functional Questions for Later Design

Before development begins, the team must answer:

- Which ERPNext DocTypes can be reused?
- Which EPC objects require custom DocTypes?
- Which processes require workflows?
- Which approvals are mandatory?
- Which users can create each record?
- Which users can approve each record?
- Which records are project-specific?
- Which records require revisions?
- Which records require attachments?
- Which records require audit history?
- Which processes require notifications?
- Which processes require escalation?
- Which information should appear on dashboards?
- Which reports are required?
- Which data must be integrated with Finance?
- Which data must be integrated with Inventory?
- Which data must be integrated with Projects?

These questions will be answered in later design documents.

---

# 52. Functional Requirements Summary

The EPC ERP System must provide functionality for:

**Project Management**

→ Manage EPC projects and project structures.

**Engineering**

→ Manage technical deliverables, reviews, revisions, and approvals.

**Procurement**

→ Manage requirements, RFQs, quotations, evaluations, and Purchase Orders.

**Material**

→ Track materials from requirement through receipt, allocation, and issue.

**Construction**

→ Manage work packages, activities, and progress.

**Quality**

→ Manage inspections, tests, NCRs, and corrective actions.

**HSE**

→ Manage risks, incidents, observations, and corrective actions.

**Planning**

→ Manage schedules, dependencies, baselines, and forecasts.

**Cost**

→ Track budgets, commitments, actuals, and variance.

**Risk**

→ Identify, assess, mitigate, and monitor risks.

**Change**

→ Control technical, commercial, cost, and schedule changes.

**Document Control**

→ Manage documents, revisions, approvals, and traceability.

**Commissioning**

→ Track testing and commissioning readiness.

**Handover**

→ Manage completion and handover packages.

**Reporting**

→ Provide operational and management visibility.

---

# 53. Relationship With Previous Documents

## Document 00

`00_Business_Requirements_and_Domain_Model.md`

Defines the business problem and domain foundation.

## Document 01

`01_Project_Overview.md`

Defines the project objectives, scope, technology, and overall direction.

## Document 02

`02_Domain_Study_EPC.md`

Explains the EPC domain and its major business functions.

## Document 03

`03_Business_Process_Model.md`

Explains how the EPC business processes operate and interact.

## Document 04

`04_Functional_Requirements.md`

Defines what the software must actually do to support those business processes.

The progression is:

**Business Requirements**

↓

**Project Overview**

↓

**EPC Domain Study**

↓

**Business Process Model**

↓

**Functional Requirements**

↓

**Non-Functional Requirements**

↓

**Use Cases**

↓

**System Architecture**

↓

**Data Model**

↓

**ERPNext Capability Mapping**

↓

**Frappe Architecture**

↓

**DocType Design**

↓

**Workflow Design**

↓

**Permission Design**

↓

**UI / UX Design**

↓

**Development**

---

# 54. Current Project State

**Project Phase:** Pre-Development / System Design

**Current Stage:** Functional Requirements

The project has not yet moved into full application development.

The current objective is to establish a complete understanding of:

- EPC business processes
- Functional requirements
- Data requirements
- Workflow requirements
- User requirements
- ERPNext capabilities
- Frappe customization requirements

Development should begin only after the important design decisions have been documented and reviewed.

---

# 55. Next Step

The next documentation stage is:

**05 — Non-Functional Requirements**

This will define requirements related to:

- Performance
- Security
- Scalability
- Availability
- Reliability
- Maintainability
- Usability
- Auditability
- Data protection
- Backup and recovery
- Integration
- Monitoring
- Deployment
- System architecture constraints

The overall design progression remains:

**Understand EPC**

→ **Understand Processes**

→ **Define Functional Requirements**

→ **Define Non-Functional Requirements**

→ **Design the System**

→ **Map ERPNext**

→ **Design Frappe Customization**

→ **Develop**

→ **Test**

→ **Deploy**

→ **Maintain**

---

# 56. Final Objective

The objective of this document is to establish a clear functional contract between the EPC business requirements and the future software system.

The system should not simply provide screens for EPC users.

It should support the complete business lifecycle:

**Contract**

→ **Project**

→ **Engineering**

→ **Procurement**

→ **Material**

→ **Construction**

→ **Quality**

→ **HSE**

→ **Planning**

→ **Cost**

→ **Risk**

→ **Change**

→ **Commissioning**

→ **Handover**

→ **Closure**

The fundamental development principle is:

**Understand the Business → Model the Process → Define Requirements → Design the System → Map ERPNext → Customize Frappe Where Required → Develop → Test → Deploy**

**Document Status:** Draft

**Version:** 1.0

**Current Stage:** Functional Requirements Definition

