# 17. Client Project Brief

## ShopEase E-Commerce Management System

### Document Information

| Field | Details |
|---|---|
| Project Name | ShopEase E-Commerce Management System |
| Document Type | Client Project Brief |
| Project Reference | SE-ECOM-2026-001 |
| Business Domain | E-Commerce and Retail |
| Project Category | Web Application |
| Prepared By | Vansh Patel |
| Role | Business Analyst — Portfolio Project |
| Version | 1.0 |
| Date | October 2026 |
| Document Status | Draft — For Stakeholder Review |
| Scenario Type | Simulated Client Scenario |

> **Important Notice:** ShopEase is a fictional business created for an
> independent portfolio project. This document simulates a client brief
> for learning and demonstration purposes. It does not represent a real
> client engagement.

---

## 1. Project Background

ShopEase is a fictional retail business planning to establish an online
shopping platform to improve its product sales and order management
processes.

In the proposed business scenario, the company currently manages product
information, customer orders, and inventory records using spreadsheets
and manual communication.

As the business grows, these processes may become difficult to maintain.
The business wants to introduce a centralized web application that
allows customers to browse products and place orders while enabling
administrators to manage products, inventory, and orders.

The Business Analyst's responsibility is to understand the business
problem, identify stakeholder needs, document requirements, analyze
existing processes, and support the development and validation of
the proposed solution.

---

## 2. Business Problem

The current business scenario identifies several potential operational
problems.

### 2.1 Product Management

Product details, prices, and stock quantities are maintained manually.
This may lead to outdated information and inconsistent product records.

### 2.2 Order Processing

Orders may be received through phone calls or manual communication.
Employees must record order details and verify product availability.

### 2.3 Inventory Management

Inventory records may not be updated immediately after an order is placed.
This creates a risk of accepting orders for unavailable products.

### 2.4 Customer Communication

Customers may need to contact the business to obtain order updates.

### 2.5 Business Reporting

Management may lack a centralized view of order volumes, sales totals,
and product performance.

These problems are assumptions within the simulated scenario. They would
need to be confirmed through stakeholder interviews in an actual project.

---

## 3. Business Objectives

The proposed solution aims to achieve the following objectives.

| ID | Objective | Expected Outcome |
|---|---|---|
| OBJ-01 | Centralize product management | Product information is maintained in one system |
| OBJ-02 | Standardize order processing | Orders follow a defined workflow |
| OBJ-03 | Improve inventory consistency | Stock availability is validated before order acceptance |
| OBJ-04 | Improve customer experience | Customers can browse products and view order status |
| OBJ-05 | Support business monitoring | Administrators can review basic order and sales summaries |
| OBJ-06 | Improve data quality | Input validation and business rules reduce invalid records |

These are proposed objectives, not confirmed business results.

---

## 4. Client Expectations

For this simulated engagement, the business stakeholder expects the
proposed system to support the following capabilities.

### 4.1 Customer Capabilities

- Browse available products.
- Search for products.
- View product descriptions and prices.
- Add products to a shopping cart.
- Update quantities or remove cart items.
- Place an order.
- Receive an order confirmation.
- View order history.
- Track order status.

### 4.2 Administrator Capabilities

- Create product records.
- Update product details and prices.
- Activate or deactivate products.
- Maintain inventory quantities.
- View customer orders.
- Update order status.
- Review basic sales and order summaries.

### 4.3 Business Manager Capabilities

- Review order volumes.
- View basic sales summaries.
- Identify frequently ordered products.
- Monitor the overall order workflow.

The precise requirements and priorities must be confirmed before
implementation.

---

## 5. Existing Process — AS-IS

The following process represents the assumed current workflow.

1. A customer contacts the business to enquire about a product.
2. An employee provides product information.
3. The customer communicates the requested products and quantities.
4. The employee checks stock records.
5. The employee records the order manually.
6. The employee communicates order confirmation.
7. Staff update inventory and order records.
8. The customer contacts the business for subsequent updates.

### Potential Issues

- Repeated manual data entry.
- Delays in confirming product availability.
- Inconsistent order records.
- Difficulty tracking order progress.
- Additional administrative effort.

### AS-IS Process Summary

**Customer Enquiry → Product Verification → Manual Order Recording → Order Confirmation → Manual Inventory Update**

This workflow is a conceptual representation of the fictional business,
not an observed process from an actual company.

---

## 6. Proposed Process — TO-BE

The proposed application will support a more centralized workflow.

1. The customer opens the e-commerce application.
2. The customer browses or searches for products.
3. The customer selects products and adds them to the cart.
4. The system validates the cart and available stock.
5. The customer submits the order.
6. The system validates the order information.
7. The system creates the order and updates inventory consistently.
8. The system displays an order confirmation.
9. The customer views order status through the application.
10. An authorized administrator manages order progress.
11. The business reviews available order and sales summaries.

### TO-BE Process Summary

**Browse Products → Add to Cart → Validate Stock → Place Order → Confirm Order → Manage Order → Track Status**

The final workflow will be confirmed during requirements analysis and
implemented according to the approved prototype scope.

---

## 7. High-Level Functional Requirements

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-001 | The system shall display available products | Must Have |
| FR-002 | The system shall allow customers to search for products | Should Have |
| FR-003 | The system shall display product details and prices | Must Have |
| FR-004 | The system shall allow customers to manage cart items | Must Have |
| FR-005 | The system shall validate order quantities | Must Have |
| FR-006 | The system shall allow customers to submit valid orders | Must Have |
| FR-007 | The system shall generate a unique order identifier | Must Have |
| FR-008 | The system shall maintain order status | Must Have |
| FR-009 | Authorized administrators shall manage product records | Must Have |
| FR-010 | Authorized administrators shall manage inventory | Must Have |
| FR-011 | Authorized administrators shall update order status | Must Have |
| FR-012 | Customers shall be able to view their order history | Should Have |
| FR-013 | The system should provide basic sales summaries | Should Have |

These requirements are preliminary and must be refined before development.

---

## 8. Non-Functional Expectations

The proposed application should address the following quality attributes.

### 8.1 Usability

The interface should be understandable and easy to navigate.

### 8.2 Performance

Common operations, such as opening product listings and updating a cart,
should complete within an agreed response time under defined test conditions.

### 8.3 Security

Administrative functions must require appropriate authorization.
Sensitive information must be protected.

### 8.4 Reliability

The system should maintain consistent order and inventory information
during supported operations.

### 8.5 Maintainability

The application should use a clear structure that supports future
changes and troubleshooting.

### 8.6 Compatibility

The interface should be usable on commonly supported desktop and mobile
screen sizes.

Specific measurable targets will be defined during detailed requirements
analysis.

---

## 9. Project Scope

### 9.1 In Scope

- Product catalogue.
- Product details.
- Product search.
- Shopping cart.
- Order creation.
- Order confirmation.
- Order history and status.
- Administrator product management.
- Inventory validation.
- Order management.
- Basic sales summaries.
- Input validation.
- Requirements documentation.
- Prototype testing.
- Defect documentation.

### 9.2 Out of Scope

- Real payment gateway integration.
- Actual financial transactions.
- Live courier integrations.
- Enterprise ERP integrations.
- Multi-vendor marketplace management.
- Production deployment for real customers.
- Migration of real customer records.
- Advanced AI-based product recommendations.

The initial prototype may use simulated data and payment confirmation.
Such simulations must not be presented as real payment processing.

---

## 10. Stakeholder Register

| Stakeholder ID | Stakeholder | Responsibility | Interest |
|---|---|---|---|
| STK-01 | Customer | Browse and order products | Ease of use and order visibility |
| STK-02 | Administrator | Manage products and orders | Operational accuracy |
| STK-03 | Business Manager | Review business performance | Sales and order information |
| STK-04 | Business Analyst | Analyze and document requirements | Requirement quality and traceability |
| STK-05 | Developer | Implement application functionality | Clear, feasible requirements |
| STK-06 | Tester | Verify system functionality | Testability and quality |

The stakeholder roles are proposed for this case study. No real stakeholder
interviews or approvals are claimed.

---

## 11. Business Analyst Responsibilities

The following responsibilities define the planned BA activities for
this project.

### Requirement Elicitation

Identify the information needed to understand customer and business needs.

### Requirement Analysis

Analyze business problems, workflows, dependencies, and potential gaps.

### Requirement Documentation

Prepare business requirements, functional requirements, user stories,
acceptance criteria, and business rules.

### Process Modelling

Document the current and proposed workflows using process diagrams.

### Stakeholder Analysis

Identify stakeholder roles, interests, and expected responsibilities.

### Requirements Traceability

Map requirements to user stories and test cases using the
Requirements Traceability Matrix.

### Testing Support

Prepare UAT scenarios and evaluate whether implemented functionality
meets defined acceptance criteria.

### Change Management

Document proposed requirement changes and analyze their potential impact.

These activities describe the intended project workflow, not employment
with a real client.

---

## 12. Questions for Stakeholder Clarification

A Business Analyst should clarify important business decisions before
finalizing requirements.

### 12.1 Business Questions

1. What is the primary business problem the system must solve?
2. Which business processes currently take the most time?
3. What business outcomes are most important?
4. How will project success be measured?
5. Which features are essential for the first release?

### 12.2 Product Questions

1. What information must each product record contain?
2. Can a product have multiple categories?
3. Should inactive products appear in search results?
4. Should products have images, descriptions, and discount prices?
5. Who is authorized to update product information?

### 12.3 Inventory Questions

1. How should available stock be calculated?
2. When should inventory be reduced?
3. What should happen when two customers attempt to purchase the
   last available item?
4. Should administrators receive low-stock alerts?
5. What happens if an order is cancelled?

### 12.4 Order Management Questions

1. What information is mandatory to place an order?
2. Which order statuses are required?
3. Who can change an order status?
4. Can customers cancel an order?
5. How should failed order submissions be handled?

### 12.5 Payment Questions

1. Is payment required during order placement?
2. Which payment methods would be supported in a future release?
3. Should the initial prototype use simulated payments?
4. How should payment failures affect order status?

For the initial prototype, real payment processing is outside scope.

### 12.6 Reporting Questions

1. Which sales indicators are most useful to management?
2. Should reports be filtered by date?
3. Should administrators be able to export reports?
4. Which products should appear in product-performance summaries?

### 12.7 Security Questions

1. Which user roles are required?
2. Which operations require administrator access?
3. What customer information should be stored?
4. What protections are needed for customer information?

These questions form a proposed stakeholder discovery checklist. Their
answers must be documented before the related requirements are finalized.

---

## 13. Initial Risks and Dependencies

| ID | Risk or Dependency | Potential Impact | Proposed Action |
|---|---|---|---|
| RD-01 | Incomplete requirements | Rework and missing functionality | Conduct structured requirements reviews |
| RD-02 | Incorrect stock calculations | Orders may exceed available inventory | Define and test inventory rules |
| RD-03 | Unclear order status transitions | Inconsistent order handling | Document permitted status changes |
| RD-04 | Unauthorized administration | Potential data modification | Define roles and test access controls |
| RD-05 | Scope expansion | Increased development effort | Maintain a prioritized backlog |
| RD-06 | Inconsistent requirements and tests | Incomplete verification | Maintain requirements traceability |

These are preliminary risks identified for the simulated project.

---

## 14. Proposed Deliverables

The planned deliverables are:

1. Business Case and Project Charter.
2. Client Project Brief.
3. Stakeholder Analysis.
4. Business Requirements Document.
5. Functional Requirements Document.
6. Non-Functional Requirements.
7. User Stories and Acceptance Criteria.
8. Business Process Flows.
9. Gap Analysis.
10. UAT Test Cases.
11. Requirements Traceability Matrix.
12. Risks and Assumptions Register.
13. Agile Sprint Plan.
14. UI Wireframe Requirements.
15. Working E-Commerce Prototype.
16. Executed Test Results and Defect Log.
17. Final Project Report.

Existing documentation will be reused where appropriate. Implementation
and testing deliverables will be completed as the project progresses.

---

## 15. Proposed Delivery Plan

| Phase | Activities | Deliverable |
|---|---|---|
| Phase 1 | Define business problem and scope | Business case and project brief |
| Phase 2 | Analyze stakeholder needs | Stakeholder analysis |
| Phase 3 | Define requirements | BRD, FRD, and business rules |
| Phase 4 | Model workflows | Process flows and gap analysis |
| Phase 5 | Design the solution | UI wireframes and data design |
| Phase 6 | Build the prototype | Working application |
| Phase 7 | Test the prototype | Test results and defect log |
| Phase 8 | Review project evidence | Final project report |

The schedule and phase completion dates will be established after
estimating the implementation effort.

---

## 16. Acceptance and Review Criteria

The proposed project deliverables will be reviewed against the following
criteria:

- Requirements are clear and individually identifiable.
- Business rules are documented.
- User stories contain testable acceptance criteria.
- Process flows represent the intended business workflow.
- Requirements are linked to relevant test cases.
- Implemented features are tested against their acceptance criteria.
- Actual test results are recorded.
- Identified defects and limitations are documented.
- The final report distinguishes completed work from planned work.

Acceptance will be recorded only after the relevant review or testing
activity has been completed.

---

## 17. Business Analyst Deliverable Checklist

| Deliverable | Planned Status |
|---|---|
| Business Case and Project Charter | Documented |
| Client Project Brief | Documented |
| Stakeholder Analysis | Existing document |
| Business Requirements | Existing document |
| Functional Requirements | Existing document |
| Non-Functional Requirements | Existing document |
| User Stories | Existing document |
| Acceptance Criteria | Existing document |
| Business Process Flow | Existing document |
| Gap Analysis | Existing document |
| UAT Test Cases | Prepared; execution pending |
| Requirements Traceability Matrix | Existing document |
| Risks and Assumptions | Existing document |
| Agile Sprint Planning | Existing document |
| UI Wireframe Requirements | Existing document |
| Working Software Prototype | Planned |
| Executed Test Report | Pending implementation and testing |

Statuses should be updated when the corresponding work is completed.

---

## 18. Conclusion

This client-style project brief establishes the business context and
initial expectations for the proposed ShopEase E-Commerce Management System.

It identifies the assumed business problem, proposed solution, stakeholder
roles, preliminary requirements, scope, risks, and clarification questions.

The next phase is to validate and refine the requirements, design the
application, and implement a working prototype.

The project will provide portfolio evidence of structured Business
Analysis practices while clearly distinguishing the simulated client
scenario from actual client work.

---

## 19. Related Documents

- [Business Case and Project Charter](16_Business_Case_and_Project_Charter.md)
- [Project Overview](01_Project_Overview.md)
- [Stakeholder Analysis](02_Stakeholder_Analysis.md)
- [Business Requirements](03_Business_Requirements.md)
- [Functional Requirements](04_Functional_Requirements.md)
- [Non-Functional Requirements](05_Non_Functional_Requirements.md)
- [User Stories](06_User_Stories.md)
- [Acceptance Criteria](07_Acceptance_Criteria.md)
- [Business Process Flow](08_Business_Process_Flow.md)
- [Gap Analysis](09_Gap_Analysis.md)
- [UAT Test Cases](10_UAT_Test_Cases.md)
- [Requirements Traceability Matrix](11_Requirements_Traceability_Matrix.md)
- [Risks and Assumptions](12_Risks_and_Assumptions.md)
- [Agile Sprint Planning](13_Agile_Sprint_Planning.md)
- [Project Conclusion](14_Project_Conclusion.md)
- [UI Wireframe Requirements](15_UI_Wireframe_Requirements.md)

---

**Document Status:** Draft — Simulated Client Scenario

**Version:** 1.0

**Prepared By:** Vansh Patel
