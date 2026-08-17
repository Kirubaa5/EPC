# 01 — Project Overview

**Project Name:** EPC ERP System  
**Domain:** Engineering, Procurement & Construction (EPC)  
**Platform:** ERPNext + Frappe Framework  
**Technology:** Python, JavaScript, HTML, CSS, MariaDB, Git/GitHub  
**Document Status:** Draft  
**Version:** 1.0  
**Current Phase:** Pre-Development / Documentation & System Design

---

## 1. Project Introduction

The EPC ERP System is an integrated enterprise software platform designed to manage the complete lifecycle of Engineering, Procurement & Construction (EPC) projects.

The system will be built using ERPNext and the Frappe Framework.

The primary objective is to create a centralized platform that connects the major business functions involved in EPC project execution.

The system will bring together:

- Project Management
- Contract Management
- Engineering
- Procurement
- Vendor Management
- Material Management
- Construction
- Quality Management
- HSE Management
- Planning & Scheduling
- Cost Management
- Risk Management
- Change Management
- Document Control
- Commissioning
- Project Handover
- Reporting
- Dashboards
- Workflow and Approval Management

The system should not operate as a collection of disconnected modules.

Instead, the major business processes should be connected so that information can flow from one stage of the project to another.

---

## 2. Project Vision

The vision is to build an integrated EPC ERP platform that provides a single source of truth for project information and business operations.

The system should allow an organization to manage EPC projects from initial project creation through final handover and closure.

### High-Level Vision

EPC ERP System

→ Engineering  
→ Procurement  
→ Construction  
→ Quality  
→ HSE  
→ Project Controls  
→ Commissioning  
→ Handover  
→ Project Closure

### Long-Term Digital Vision

Manual Processes  
→ Digital Records  
→ Integrated ERP  
→ Workflow Automation  
→ Real-Time Visibility  
→ Analytics  
→ Predictive Intelligence  
→ AI-Assisted EPC Management

---

## 3. Why This Project Is Required

EPC projects are complex and involve large amounts of information.

A single project can contain:

- Engineering drawings
- Technical specifications
- Material requirements
- Purchase orders
- Vendor information
- Construction activities
- Inspection records
- Quality records
- HSE records
- Project schedules
- Cost information
- Contract information
- Client communications
- Approvals
- Project reports
- Thousands of project documents

When this information is managed through disconnected systems, spreadsheets, emails, and manual processes, several problems can occur.

Common problems include:

- Data duplication
- Data inconsistency
- Manual data entry
- Delayed information
- Approval delays
- Poor document control
- Difficult revision tracking
- Poor procurement visibility
- Poor material visibility
- Cost control problems
- Schedule visibility problems
- Communication gaps
- Difficult reporting
- Lack of end-to-end traceability

The EPC ERP System is intended to reduce these problems by integrating the major EPC processes into one platform.

---

## 4. Project Objectives

The project has the following primary objectives.

### 4.1 Centralize Project Information

Create one centralized platform for project-related information.

### 4.2 Integrate EPC Departments

Connect:

- Engineering
- Procurement
- Construction
- Quality
- HSE
- Planning
- Cost Control
- Document Control
- Commissioning

### 4.3 Improve Project Visibility

Provide users and management with visibility into:

- Project progress
- Engineering progress
- Procurement status
- Material status
- Construction progress
- Quality status
- HSE status
- Cost performance
- Schedule performance
- Risk status

### 4.4 Improve Traceability

Users should be able to trace important transactions from their origin to completion.

Example:

Engineering Requirement  
→ Material Requirement  
→ Purchase Requisition  
→ RFQ  
→ Vendor Quotation  
→ Evaluation  
→ Purchase Order  
→ Delivery  
→ Receipt  
→ Inspection  
→ Construction

### 4.5 Reduce Manual Work

The system should reduce repetitive manual activities through:

- Workflows
- Notifications
- Automated validations
- Scheduled processes
- Reports
- Dashboards

### 4.6 Improve Decision Making

Provide reliable information for:

- Project managers
- Department heads
- Project controls
- Finance
- Senior management

---

## 5. Project Scope

The project covers the major business functions required to manage EPC projects.

The initial scope includes:

1. Project Management
2. Contract Management
3. Engineering Management
4. Procurement Management
5. Vendor Management
6. Material Management
7. Construction Management
8. Quality Management
9. HSE Management
10. Planning & Scheduling
11. Cost Management
12. Risk Management
13. Change Management
14. Document Control
15. Commissioning
16. Project Handover
17. Reporting
18. Dashboards
19. Workflow and Approval Management

---

## 6. Project Management

The Project Management domain will manage the overall project.

It may include:

- Project creation
- Project identification
- Project scope
- Project status
- Project phases
- Project team
- Project manager
- Project milestones
- Project locations
- Project progress
- Project reporting
- Project closure

The project should act as the central context connecting different EPC processes.

---

## 7. Contract Management

Contract Management will manage contractual information related to projects.

It may include:

- Client contracts
- Contract number
- Contract value
- Contract scope
- Contract dates
- Contract milestones
- Contract documents
- Contract obligations
- Variations
- Claims
- Contract status

Contract information should be connected with relevant project activities.

---

## 8. Engineering Management

Engineering is one of the major EPC functions.

The Engineering domain may manage:

- Engineering disciplines
- Engineering requirements
- Engineering deliverables
- Drawings
- Specifications
- Datasheets
- Calculations
- Technical reports
- Engineering documents
- Document revisions
- Engineering reviews
- Engineering approvals

Typical engineering disciplines may include:

- Process
- Civil
- Structural
- Mechanical
- Electrical
- Instrumentation
- Piping
- Architecture
- Other specialized disciplines

Engineering outputs can become inputs for procurement and construction.

Engineering  
→ Approved Engineering Information  
→ Procurement / Construction

---

## 9. Procurement Management

Procurement converts project requirements into purchased goods and services.

The procurement lifecycle may include:

Requirement  
→ Purchase Requisition  
→ RFQ  
→ Vendor Quotation  
→ Technical Evaluation  
→ Commercial Evaluation  
→ Approval  
→ Purchase Order  
→ Vendor Execution  
→ Inspection  
→ Shipment  
→ Delivery  
→ Receipt

The system should provide traceability throughout this process.

---

## 10. Vendor Management

Vendor Management will maintain information about organizations supplying materials, equipment, or services.

It may include:

- Vendor registration
- Vendor master data
- Vendor qualification
- Vendor evaluation
- Vendor documents
- Vendor status
- Vendor performance
- Vendor history

Vendor performance may later be used for analytics.

---

## 11. Material Management

Material Management will manage materials and equipment required for project execution.

It may include:

- Material master
- Material categories
- Material specifications
- Units of measure
- Material requirements
- Material availability
- Material delivery
- Material receipt
- Material inspection
- Material allocation
- Material status

Material information should connect engineering, procurement, inventory, quality, and construction.

---

## 12. Construction Management

Construction Management will manage physical project execution.

It may include:

- Construction planning
- Work packages
- Construction activities
- Site activities
- Resource allocation
- Material availability
- Construction progress
- Inspections
- Testing
- Punch lists
- Completion records

Construction flow:

Construction Planning  
→ Work Package  
→ Activity  
→ Resource Allocation  
→ Construction Execution  
→ Progress Recording  
→ Inspection  
→ Testing  
→ Punch List  
→ Completion

---

## 13. Quality Management

Quality Management will ensure that project activities and deliverables meet defined requirements.

The domain may include:

- Quality plans
- Inspection plans
- Inspection requests
- Inspections
- Test records
- Quality approvals
- Non-Conformance Reports
- Corrective actions
- Quality certificates
- Quality reports

Typical quality flow:

Quality Requirement  
→ Inspection Planning  
→ Inspection  
→ Testing  
→ Result  
→ Accepted / Rejected  
→ NCR if Required  
→ Corrective Action  
→ Verification  
→ Closure

---

## 14. HSE Management

HSE stands for:

- Health
- Safety
- Environment

The HSE domain may manage:

- Safety observations
- HSE inspections
- Incidents
- Near misses
- Environmental observations
- Corrective actions
- Safety records
- HSE reporting

Typical process:

HSE Planning  
→ Site Execution  
→ Observation / Inspection  
→ Incident if Applicable  
→ Investigation  
→ Corrective Action  
→ Verification  
→ Closure

---

## 15. Planning and Scheduling

Planning and Scheduling will manage project timelines and progress.

It may include:

- Project schedules
- Activities
- Milestones
- Dependencies
- Baselines
- Planned dates
- Actual dates
- Progress
- Forecast dates
- Schedule variance

Simplified flow:

Project Planning  
→ Schedule Creation  
→ Activities  
→ Dependencies  
→ Baseline  
→ Actual Progress  
→ Schedule Monitoring  
→ Variance Analysis  
→ Forecast

---

## 16. Cost Management

Cost Management will provide visibility into project financial performance.

It may include:

- Project budget
- Planned cost
- Committed cost
- Actual cost
- Forecast cost
- Cost variance
- Cost reports

Conceptual flow:

Project Budget  
→ Commitments  
→ Actual Costs  
→ Cost Monitoring  
→ Variance Analysis  
→ Forecast

---

## 17. Risk Management

Risk Management will manage potential events that may affect project objectives.

It may include:

- Risk identification
- Risk description
- Risk category
- Probability
- Impact
- Risk score
- Risk owner
- Mitigation plan
- Risk status
- Risk monitoring

Example:

Risk Identified  
→ Risk Assessment  
→ Risk Owner Assigned  
→ Mitigation Plan  
→ Monitoring  
→ Review  
→ Closed / Accepted / Escalated

---

## 18. Change Management

EPC projects may change during execution.

Changes may affect:

- Scope
- Design
- Cost
- Schedule
- Materials
- Contract
- Construction

The system should support:

- Change requests
- Change evaluation
- Impact analysis
- Approval
- Implementation
- Change history
- Contract variations

Simplified flow:

Change Request  
→ Impact Analysis  
→ Technical Review  
→ Commercial Review  
→ Approval  
→ Implementation  
→ Tracking  
→ Closure

---

## 19. Document Control

Document Control is a critical capability in EPC projects.

The system may manage:

- Document registration
- Document numbering
- Document type
- Revision
- Review
- Approval
- Distribution
- Status
- Document history

Typical document lifecycle:

Created  
→ Submitted  
→ Under Review  
→ Approved / Rejected  
→ Issued  
→ Revised  
→ Re-Review

The system should help prevent users from unknowingly using obsolete revisions.

---

## 20. Commissioning Management

Commissioning verifies whether completed systems and equipment are ready for operation.

It may include:

- Commissioning plans
- Commissioning systems
- Commissioning activities
- Testing
- Functional verification
- Performance verification
- Punch-list tracking
- Completion status

Simplified flow:

Construction Completion  
→ Pre-Commissioning  
→ Testing  
→ Verification  
→ Punch List  
→ Punch Closure  
→ Commissioning Complete

---

## 21. Project Handover

Project Handover represents the transition of the completed project or facility to the client or operational organization.

It may include:

- Handover planning
- Handover packages
- As-built documents
- Test records
- Inspection records
- Certificates
- Completion records
- Operation and maintenance documents
- Punch-list closure
- Client acceptance

Simplified flow:

Project Completion  
→ Handover Preparation  
→ Document Compilation  
→ Technical Verification  
→ Punch Closure  
→ Client Review  
→ Acceptance  
→ Handover

---

## 22. Target Users

The system will support different types of users.

### 22.1 Management

Management requires high-level visibility into:

- Projects
- Progress
- Cost
- Schedule
- Procurement
- Quality
- HSE
- Risks
- Issues

### 22.2 Project Manager

The Project Manager requires:

- Project overview
- Project progress
- Schedule
- Cost
- Risks
- Issues
- Changes
- Team activities

### 22.3 Engineering User

Engineering users require:

- Engineering tasks
- Deliverables
- Documents
- Revisions
- Reviews
- Approvals

### 22.4 Procurement User

Procurement users require:

- Requirements
- Purchase requisitions
- RFQs
- Quotations
- Evaluations
- Purchase orders
- Vendor information
- Delivery status

### 22.5 Construction User

Construction users require:

- Work packages
- Activities
- Site information
- Materials
- Progress
- Inspections
- Punch lists

### 22.6 Quality User

Quality users require:

- Inspection plans
- Inspections
- Tests
- NCRs
- Corrective actions
- Quality reports

### 22.7 HSE User

HSE users require:

- HSE inspections
- Safety observations
- Incidents
- Corrective actions
- HSE reports

### 22.8 Planner / Project Controls User

Requires:

- Schedules
- Activities
- Milestones
- Progress
- Baselines
- Forecasts
- Schedule variance

### 22.9 Cost Controller

Requires:

- Budget
- Commitments
- Actual cost
- Forecast
- Variance

### 22.10 Document Controller

Requires:

- Document registration
- Revision management
- Review tracking
- Approval tracking
- Distribution
- Document history

### 22.11 System Administrator

Responsible for:

- Users
- Roles
- Permissions
- Configuration
- Workflows
- System administration

---

## 23. High-Level Project Lifecycle

The complete EPC project lifecycle can be viewed as:

Project Award  
→ Project Initiation  
→ Project Planning  
→ Engineering Planning  
→ Engineering  
→ Procurement  
→ Construction  
→ Inspection & Testing  
→ Commissioning  
→ Handover  
→ Project Closure

However, EPC activities are not always strictly sequential.

Multiple activities may happen in parallel.

Engineering  
→ continues while Procurement begins

Procurement  
→ continues while Construction begins

Construction  
→ continues while Commissioning activities begin

This parallel nature is an important characteristic of EPC project execution.

---

## 24. Core Business Integration

One of the most important objectives of the system is to connect different EPC domains.

Example:

Engineering  
→ Approved Design  
→ Procurement  
→ Purchased Material  
→ Material Management  
→ Available Material  
→ Construction  
→ Installed  
→ Quality  
→ Accepted  
→ Commissioning  
→ Tested  
→ Handover

This means that one department's output can become another department's input.

The system should preserve these relationships and provide end-to-end traceability.

---

## 25. Cross-Cutting Capabilities

Some capabilities apply to almost every domain.

### Authentication

Users must be authenticated before accessing protected system functionality.

### Authorization

Users must only access data and actions permitted to them.

### Workflow

Business processes should have controlled state transitions.

### Notifications

Users should receive notifications for important actions and events.

### Audit Trail

Important business actions should be traceable.

### Document Management

Relevant documents should be associated with business transactions.

### Search

Users should be able to find project information efficiently.

### Reporting

Each major business domain should provide appropriate reports.

### Dashboards

Management should have high-level project visibility.

---

## 26. Technology Stack

The system will use the following technology foundation.

### Application Platform

**ERPNext**

ERPNext will provide standard ERP capabilities wherever suitable.

### Framework

**Frappe Framework**

Frappe will provide:

- DocTypes
- ORM
- Backend framework
- Permissions
- Workflows
- APIs
- Server-side logic
- Client-side scripting
- Reports
- Background jobs
- Notifications
- Web functionality

### Backend

**Python**

Python will be used for:

- Business logic
- Server-side validation
- APIs
- Automation
- Background processing
- Integrations

### Frontend

The application may use:

- HTML
- CSS
- JavaScript
- Frappe UI capabilities
- ERPNext interfaces

Custom frontend development will be introduced where required.

### Database

**MariaDB**

MariaDB will store application and business data.

### Version Control

**Git / GitHub**

Git will be used to manage:

- Source code
- Documentation
- Configuration
- Version history
- Branches

---

## 27. Repository and Documentation Structure

The project documentation will be maintained as Markdown files in the Git repository.

The planned structure is:

EPC-ERP  
→ docs  
→ 00_Business_Requirements_and_Domain_Model.md  
→ 01_Project_Overview.md  
→ 02_Stakeholders_and_User_Roles.md  
→ 03_Functional_Requirements.md  
→ ...  

The final repository structure will be defined as the project evolves.

---

## 28. ERPNext Strategy

ERPNext will be treated as the foundation rather than rebuilding a complete ERP system from scratch.

The approach is:

Business Requirement  
→ Check ERPNext Capability  
→ If Supported → Reuse ERPNext  
→ If Not Supported → Perform Gap Analysis  
→ Design Custom Frappe Feature

The project should follow:

> Reuse first, customize only when necessary.

Before creating a custom DocType or feature, the team should determine whether ERPNext already provides an appropriate capability.

---

## 29. Frappe Customization Strategy

Custom Frappe development may be required for:

- EPC-specific DocTypes
- Custom fields
- Custom business rules
- Custom validations
- Custom workflows
- Custom dashboards
- Custom reports
- Custom APIs
- Custom integrations
- EPC-specific automation
- EPC-specific document processes

Every major customization should have a documented business reason.

---

## 30. Development Approach

The project will follow a design-first approach.

The overall sequence is:

EPC Domain Understanding  
→ Business Requirements  
→ Business Process Design  
→ Functional Requirements  
→ System Architecture  
→ Data Model  
→ ERPNext Mapping  
→ Custom Frappe Design  
→ UI / UX Design  
→ Development  
→ Testing  
→ Deployment

Development should not start by randomly creating DocTypes.

The business process should be understood first.

---

## 31. Vertical Slice Development

After the design stage, implementation should preferably follow vertical business slices.

Instead of developing every DocType separately, the system should be developed through complete business flows.

For example:

Engineering Requirement  
→ Material Requirement  
→ Purchase Requisition  
→ RFQ  
→ Vendor Quotation  
→ Evaluation  
→ Purchase Order  
→ Delivery  
→ Receipt

This allows the complete business process to be developed and tested together.

---

## 32. Project Design Principles

The following principles will guide the project.

### Principle 1 — Business Before Technology

Understand the business before choosing implementation details.

### Principle 2 — Reuse Before Customize

Use ERPNext functionality wherever possible.

### Principle 3 — Integration Before Isolation

Design connected processes rather than isolated modules.

### Principle 4 — Traceability by Design

Important transactions must be traceable.

### Principle 5 — Security by Design

Permissions must be considered during system design.

### Principle 6 — Workflow by Design

Important approvals and state transitions must be explicitly modeled.

### Principle 7 — Data Quality by Design

Master data must be structured carefully.

### Principle 8 — Documentation Before Development

Important decisions should be documented before implementation.

### Principle 9 — Testable Requirements

Requirements should eventually be converted into test cases.

### Principle 10 — Incremental Development

The system should be developed and validated in manageable stages.

---

## 33. Reporting and Dashboard Vision

The system should eventually provide multiple reporting levels.

### Executive Level

Possible information:

- Total projects
- Active projects
- Project health
- Overall progress
- Cost performance
- Schedule performance
- Major risks
- Major issues

### Project Level

Possible information:

- Project progress
- Engineering progress
- Procurement progress
- Construction progress
- Cost
- Schedule
- Quality
- HSE
- Risks

### Department Level

Possible information:

- Engineering deliverables
- Procurement status
- Vendor performance
- Construction progress
- Quality records
- HSE records

### Operational Level

Possible information:

- Pending approvals
- Delayed documents
- Delayed deliveries
- Open NCRs
- Open HSE actions
- Overdue activities
- Pending inspections

---

## 34. Potential KPIs

### Project KPIs

- Overall project progress
- Planned vs actual progress
- Schedule variance
- Cost variance
- Forecast completion date

### Engineering KPIs

- Deliverables planned
- Deliverables completed
- Deliverables overdue
- Documents pending approval
- Revision count

### Procurement KPIs

- Purchase requisitions
- RFQs
- Purchase orders
- Pending orders
- Delayed deliveries
- Vendor performance

### Construction KPIs

- Planned progress
- Actual progress
- Work package completion
- Productivity
- Open punch items

### Quality KPIs

- Inspections completed
- Inspection failures
- Open NCRs
- NCR closure time

### HSE KPIs

- Incidents
- Near misses
- Safety observations
- HSE inspections
- Corrective action closure

---

## 35. Security Overview

The system will use Frappe and ERPNext security capabilities wherever appropriate.

Security will consider:

- User authentication
- Role-based permissions
- User permissions
- Document permissions
- Workflow permissions
- Data access restrictions
- Audit trails

Sensitive project information must only be accessible to authorized users.

Detailed security architecture will be documented separately.

---

## 36. Auditability

Important business actions should be traceable.

The system should allow the organization to determine:

- **Who** performed the action
- **What** was changed
- **When** it happened
- **Which project or transaction** was involved

Examples:

- Who approved the purchase order?
- Who approved the engineering document?
- Who changed the project status?
- Who closed the NCR?
- Who approved the change request?
- Who modified a controlled document?

---

## 37. Expected Benefits

### Operational Benefits

- Reduced manual work
- Faster processes
- Better coordination
- Better traceability
- Reduced duplicate data

### Management Benefits

- Better visibility
- Faster reporting
- Better decision making
- Better project control

### Financial Benefits

- Better cost visibility
- Better budget control
- Better forecasting
- Better variance analysis

### Quality Benefits

- Better inspection tracking
- Better NCR management
- Better quality traceability

### HSE Benefits

- Better incident tracking
- Better safety visibility
- Better corrective action management

### Project Benefits

- Better schedule visibility
- Better procurement visibility
- Better material tracking
- Better project coordination

---

## 38. Success Criteria

The system should eventually be capable of:

1. Creating and managing EPC projects.
2. Managing project information centrally.
3. Managing project contracts.
4. Managing engineering deliverables.
5. Managing engineering documents and revisions.
6. Connecting engineering requirements with procurement.
7. Managing procurement from requirement to delivery.
8. Managing vendors.
9. Managing materials and equipment.
10. Managing construction activities.
11. Tracking construction progress.
12. Managing inspections and testing.
13. Managing quality records.
14. Managing NCRs and corrective actions.
15. Managing HSE records.
16. Managing project schedules.
17. Managing project costs.
18. Managing project risks.
19. Managing project changes.
20. Managing project documents.
21. Supporting workflows and approvals.
22. Providing dashboards and reports.
23. Providing appropriate user permissions.
24. Maintaining auditability and traceability.
25. Supporting multiple EPC projects.

---

## 39. Future Digital Capabilities

The system should provide a foundation for future technologies.

### 39.1 Automation

Potential capabilities:

- Automatic notifications
- Automatic reminders
- Scheduled reports
- Workflow automation

### 39.2 Analytics

Potential capabilities:

- Project performance analytics
- Vendor analytics
- Cost analytics
- Schedule analytics

### 39.3 Predictive Analytics

Potential capabilities:

- Delay prediction
- Cost forecasting
- Risk prediction
- Vendor performance prediction

### 39.4 Artificial Intelligence

Potential future AI capabilities may include:

- Document intelligence
- AI-assisted document search
- AI-assisted report generation
- Project status summarization
- Risk analysis
- Delay analysis
- Procurement recommendations
- EPC knowledge assistant

These capabilities are future possibilities and should not be treated as initial implementation requirements.

---

## 40. Project Constraints

Potential constraints include:

- EPC processes differ between industries.
- Client requirements may vary.
- Contract requirements may vary.
- Regulatory requirements may vary.
- Existing systems may need integration.
- EPC projects may contain very large numbers of documents.
- Different users may require different access levels.
- Some project information may be confidential.
- External vendors may require restricted access.
- Existing organizational processes may need to be preserved.

---

## 41. Key Assumptions

The project currently assumes:

1. The system will support multiple EPC projects.
2. Projects may involve multiple departments.
3. ERPNext standard functionality will be reused where appropriate.
4. Frappe will be used for custom EPC functionality.
5. Business requirements will be validated before development.
6. The system will require role-based access control.
7. Important business transactions will require traceability.
8. Workflows will be required for controlled processes.
9. The design may evolve as the EPC domain is studied further.
10. Sector-specific requirements may be added later.

---

## 42. Project Documentation Strategy

The project will use documentation as part of the development lifecycle.

The documentation will cover:

Business  
→ Requirements  
→ Processes  
→ Use Cases  
→ Architecture  
→ Data  
→ ERPNext Mapping  
→ Frappe Design  
→ UI / UX  
→ Security  
→ Testing  
→ Deployment

Each major design decision should have a corresponding document or documented section.

---

## 43. Planned Documentation Structure

The documentation is expected to evolve approximately as follows:

- `00_Business_Requirements_and_Domain_Model.md`
- `01_Project_Overview.md`
- `02_Stakeholders_and_User_Roles.md`
- `03_Functional_Requirements.md`
- `04_Non_Functional_Requirements.md`
- `05_EPC_Business_Processes.md`
- `06_Use_Cases.md`
- `07_System_Architecture.md`
- `08_Data_Model.md`
- `09_ERPNext_Capability_Mapping.md`
- `10_Custom_Frappe_Architecture.md`
- `11_DocType_Design.md`
- `12_Workflow_Design.md`
- `13_Permission_and_Security_Design.md`
- `14_UI_UX_Design.md`
- `15_API_and_Integration_Design.md`
- `16_Reporting_and_Dashboard_Design.md`
- `17_Notification_Design.md`
- `18_Document_Management_Design.md`
- `19_Testing_Strategy.md`
- `20_Deployment_Architecture.md`
- `21_DevOps_and_Git_Strategy.md`
- `22_Monitoring_and_Maintenance.md`
- `23_Future_Enhancements.md`

This structure is a starting point and may be changed as the project design evolves.

---

## 44. Relationship With Document 00

`00_Business_Requirements_and_Domain_Model.md` establishes the business and domain foundation.

This document establishes the overall software project definition.

The relationship is:

`00_Business_Requirements_and_Domain_Model.md`

→ EPC Domain  
→ Business Foundation  
→ `01_Project_Overview.md`  
→ Project Definition

Document 00 primarily answers:

> What is EPC and what business concepts and processes exist?

Document 01 primarily answers:

> What are we building, why are we building it, who will use it, what will it cover, and how will the project be approached?

---

## 45. Current Project State

The project is currently in the:

**Pre-Development / Documentation & System Design Phase**

The current priority is to understand and document the EPC domain before implementation.

Current sequence:

EPC Domain Understanding  
→ Business Requirements Documentation  
→ Project Overview  
→ Business Process Design  
→ System Architecture  
→ Data Design  
→ ERPNext Gap Analysis  
→ UI / UX Design  
→ Development

At this stage, the final DocTypes, workflows, screens, fields, permissions, and business rules are not considered permanently fixed.

They will be refined through the design and analysis process.

---

## 46. Final Project Definition

The EPC ERP System is an integrated enterprise platform designed to manage EPC project execution from project initiation through engineering, procurement, construction, quality, HSE, commissioning, handover, and project closure.

The system will be built using:

- ERPNext
- Frappe Framework
- Python
- JavaScript
- HTML / CSS
- MariaDB
- Git / GitHub

The project will follow a:

**Design-First + Business-Process-Driven + ERPNext-Reuse-First**

approach.

The immediate objective is not to start coding.

The immediate objective is to understand the EPC domain deeply enough to design a software system that represents real EPC business processes correctly.

The overall development philosophy is:

**Understand → Document → Model → Design → Validate → Develop → Test → Deploy → Improve**

**Current State:** Pre-Development / Documentation & System Design

**Technology Foundation:** ERPNext + Frappe Framework

**Primary Goal:** Build an integrated EPC ERP system based on real EPC business processes rather than developing isolated software features.