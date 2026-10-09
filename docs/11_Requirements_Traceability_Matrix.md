# Requirements Traceability Matrix (RTM)

## 1. Purpose

The Requirements Traceability Matrix (RTM) establishes a relationship between business requirements, functional requirements, user stories, and UAT test cases.

It helps the Business Analyst track requirement coverage and identify requirements that still need validation or testing.

## 2. Traceability Matrix

| Business Requirement ID | Business Requirement                                  | Functional Requirement ID | User Story ID | UAT Test Case ID | Priority |
| ----------------------- | ----------------------------------------------------- | ------------------------- | ------------- | ---------------- | -------- |
| BR-01                   | Customers can create accounts.                        | FR-01                     | US-01         | UAT-001, UAT-002 | High     |
| BR-02                   | Customers can securely access their accounts.         | FR-02                     | US-02         | UAT-003, UAT-004 | High     |
| BR-03                   | Customers can search for products.                    | FR-05                     | US-03         | UAT-005          | High     |
| BR-04                   | Customers can view product details.                   | FR-06                     | US-04         | UAT-006          | Medium   |
| BR-05                   | Customers can add products to a shopping cart.        | FR-10                     | US-05         | UAT-007          | High     |
| BR-06                   | Customers can update or remove cart items.            | FR-11, FR-12              | US-06         | UAT-008, UAT-009 | High     |
| BR-07                   | Customers can review the order total before checkout. | FR-13                     | US-07         | UAT-011          | High     |
| BR-08                   | Customers can submit orders through checkout.         | FR-14, FR-15              | US-08         | UAT-010          | High     |
| BR-09                   | Customers can pay using a supported payment method.   | FR-16, FR-17              | US-09         | UAT-012, UAT-013 | High     |
| BR-10                   | Customers receive order confirmation.                 | FR-18                     | US-10         | UAT-014          | High     |
| BR-11                   | Customers can track their orders.                     | FR-20                     | US-11         | UAT-015          | Medium   |
| BR-12                   | Administrators can manage products and orders.        | FR-24, FR-25              | US-13, US-14  | UAT-016, UAT-017 | High     |

**Important:** This is an initial traceability matrix for the practice project. Verify every requirement ID against the corresponding BRD, FRD, and user story documents before treating the matrix as final.

## 3. Traceability Benefits

* **Requirement coverage:** Helps ensure that business needs are represented in the system requirements.
* **Testing coverage:** Connects requirements to planned UAT test cases.
* **Change management:** Helps identify related documents and tests when a requirement changes.
* **Gap identification:** Highlights requirements that may not yet have a corresponding test case.
* **Stakeholder communication:** Provides a shared view of requirements and their validation status.

## 4. Change Impact Analysis

When a requirement changes, the Business Analyst should:

1. Identify the affected business requirement.
2. Review the linked functional requirements.
3. Identify affected user stories and acceptance criteria.
4. Update relevant UAT test cases.
5. Confirm the impact with stakeholders and the development team.
6. Update the RTM and maintain document consistency.

## 5. Current Status

| Activity                           | Status                      |
| ---------------------------------- | --------------------------- |
| Business requirements documented   | Completed as a draft        |
| Functional requirements documented | Completed as a draft        |
| User stories documented            | Completed as a draft        |
| UAT test cases prepared            | Prepared; execution pending |
| Requirements mapped in RTM         | Initial mapping prepared    |
| Stakeholder approval               | Pending                     |

## 6. Expected Outcome

The RTM provides a structured view of requirement coverage and supports requirement validation, change management, and UAT planning throughout the project lifecycle.
