# Project Risks and Assumptions Register

## 1. Purpose

This document identifies potential risks, assumptions, and dependencies associated with the proposed e-commerce system.

The objective is to identify possible issues early and recommend actions to reduce their impact on project delivery and business operations.

**Note:** This is an academic practice project. The risks and assumptions below are illustrative and should be validated with actual stakeholders in a real project.

## 2. Risk Register

| Risk ID | Risk Description                                                 | Probability | Impact | Priority | Mitigation Strategy                                                              |
| ------- | ---------------------------------------------------------------- | ----------- | ------ | -------- | -------------------------------------------------------------------------------- |
| R-01    | Payment gateway integration may experience technical issues.     | Medium      | High   | High     | Validate the integration requirements and test payment scenarios before release. |
| R-02    | Customer information may be exposed through unauthorized access. | Low         | High   | High     | Apply appropriate access controls, secure data handling, and security testing.   |
| R-03    | Incorrect product prices may appear during checkout.             | Medium      | High   | High     | Validate pricing rules and test order-total calculations.                        |
| R-04    | Product availability may not be updated accurately.              | Medium      | High   | High     | Define inventory update rules and test stock-availability scenarios.             |
| R-05    | Requirements may change during development.                      | Medium      | Medium | Medium   | Maintain version-controlled documentation and assess the impact of each change.  |
| R-06    | Users may find the checkout process difficult to understand.     | Medium      | Medium | Medium   | Review the checkout workflow and conduct usability testing.                      |
| R-07    | Order confirmation notifications may fail.                       | Medium      | Medium | Medium   | Test notification scenarios and define appropriate error handling.               |
| R-08    | Incomplete testing may allow defects into production.            | Medium      | High   | High     | Prepare test cases, prioritize critical workflows, and track unresolved defects. |

## 3. Risk Assessment Method

Risk priority is assessed using the probability of occurrence and the potential business impact.

* **High:** Requires priority attention and a mitigation plan.
* **Medium:** Requires monitoring and appropriate preventive action.
* **Low:** Can be monitored through normal project activities.

The assessments are preliminary and should be reviewed with project stakeholders.

## 4. Assumptions Register

| Assumption ID | Assumption                                                                 | Validation Method                                                                       |
| ------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| A-01          | Customers will have access to a compatible device and internet connection. | Confirm target-user and system-access requirements.                                     |
| A-02          | Customers will provide valid registration and delivery information.        | Define input-validation and checkout requirements.                                      |
| A-03          | Product names, prices, and availability will be maintained accurately.     | Confirm product-management responsibilities and data rules.                             |
| A-04          | A suitable payment gateway will be available for integration.              | Confirm provider capabilities, supported payment methods, and integration requirements. |
| A-05          | Administrators will have permission to manage products and orders.         | Confirm administrator roles and access permissions.                                     |
| A-06          | Business stakeholders will review and approve documented requirements.     | Agree on a requirements-review and approval process.                                    |
| A-07          | The system will provide order-status information to customers.             | Confirm the required order statuses and update rules.                                   |

## 5. Project Dependencies

| Dependency ID | Dependency                                                       | Potential Impact                                    |
| ------------- | ---------------------------------------------------------------- | --------------------------------------------------- |
| D-01          | Payment gateway availability and integration documentation       | May affect checkout and payment processing.         |
| D-02          | Accurate product and inventory data                              | May affect product availability and order accuracy. |
| D-03          | Stakeholder availability                                         | May affect requirement clarification and approval.  |
| D-04          | Development and testing environments                             | May affect implementation and UAT execution.        |
| D-05          | Notification service availability, if notifications are required | May affect order-confirmation communication.        |

## 6. Business Analyst Responsibilities

The Business Analyst should:

1. Identify and document potential risks and assumptions.
2. Clarify uncertain requirements with stakeholders.
3. Evaluate the business impact of identified risks.
4. Recommend mitigation actions.
5. Track changes to risks, assumptions, and dependencies.
6. Communicate significant issues to the project team.
7. Update project documentation when new information becomes available.

## 7. Expected Outcome

This register provides a structured approach to identifying project uncertainties, planning mitigation actions, and supporting informed decision-making throughout the e-commerce project lifecycle.
