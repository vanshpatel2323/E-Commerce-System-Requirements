# User Acceptance Testing (UAT) Test Cases

## 1. Purpose

The purpose of User Acceptance Testing (UAT) is to verify that the proposed e-commerce system meets business requirements and supports the expected customer and administrator workflows.

These test cases are prepared for an academic practice project. They describe expected results and have not yet been executed against a working application.

## 2. Testing Scope

UAT covers the following functional areas:

* Customer registration and login
* Product search and selection
* Shopping cart
* Checkout and order total
* Payment processing
* Order confirmation
* Order tracking
* Product and order administration

## 3. Test Environment

| Item         | Description                              |
| ------------ | ---------------------------------------- |
| Application  | E-Commerce System                        |
| Testing Type | User Acceptance Testing                  |
| Test Data    | Sample customer, product, and order data |
| Tester       | Business Analyst / Business User         |
| Status       | Not Executed                             |

## 4. UAT Test Cases

| Test Case ID | Test Scenario               | Test Steps                                                      | Expected Result                                                                       | Priority |
| ------------ | --------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------------- | -------- |
| UAT-001      | Customer registration       | Enter valid customer details and submit the registration form.  | Account is created and a confirmation is displayed.                                   | High     |
| UAT-002      | Invalid registration        | Submit registration with missing required information.          | Validation messages identify the missing information.                                 | High     |
| UAT-003      | Customer login              | Enter valid login credentials.                                  | Customer successfully accesses the account.                                           | High     |
| UAT-004      | Invalid login               | Enter incorrect login credentials.                              | Access is denied and an appropriate error message is displayed.                       | High     |
| UAT-005      | Product search              | Search for an existing product by name.                         | Relevant matching products are displayed.                                             | High     |
| UAT-006      | Product details             | Select a product from the results.                              | Product details, price, and availability are displayed.                               | Medium   |
| UAT-007      | Add to cart                 | Add an available product to the shopping cart.                  | The selected product appears in the cart.                                             | High     |
| UAT-008      | Update cart quantity        | Change the quantity of a product in the cart.                   | Quantity and order total are updated correctly.                                       | High     |
| UAT-009      | Remove from cart            | Remove a product from the cart.                                 | The product is removed and the order total is recalculated.                           | Medium   |
| UAT-010      | Checkout validation         | Attempt checkout without completing required information.       | The system requests the missing information.                                          | High     |
| UAT-011      | Order total                 | Add products with known prices to the cart.                     | The system calculates the correct order total according to the defined pricing rules. | High     |
| UAT-012      | Successful payment          | Complete checkout using a valid test payment method.            | Successful payment is recorded and the order is created according to business rules.  | High     |
| UAT-013      | Failed payment              | Simulate a declined payment using an approved test environment. | The failure is communicated and the order is not incorrectly marked as paid.          | High     |
| UAT-014      | Order confirmation          | Complete a successful order.                                    | An order confirmation with an order reference is displayed.                           | High     |
| UAT-015      | Order tracking              | Open an existing order.                                         | The customer can view the available order status.                                     | Medium   |
| UAT-016      | Admin product management    | An authorized administrator adds a product.                     | The product is saved and displayed according to business rules.                       | High     |
| UAT-017      | Admin order management      | An authorized administrator opens an order.                     | The administrator can view the relevant order details.                                | High     |
| UAT-018      | Unauthorized administration | A customer attempts to access an administrator-only feature.    | Access is denied.                                                                     | High     |

## 5. Test Execution Results

Test results must be recorded when the application is available for testing.

| Test Case ID | Actual Result | Status       | Defect Reference |
| ------------ | ------------- | ------------ | ---------------- |
| UAT-001      | Not tested    | Not Executed | N/A              |
| UAT-002      | Not tested    | Not Executed | N/A              |
| UAT-003      | Not tested    | Not Executed | N/A              |
| UAT-004      | Not tested    | Not Executed | N/A              |
| UAT-005      | Not tested    | Not Executed | N/A              |

The remaining test cases will be recorded in the same format during execution.

## 6. Defect Management

If a test fails:

1. Record the test case ID.
2. Describe the actual behaviour.
3. Compare it with the expected result.
4. Record the defect and its severity.
5. Share the issue with the development team.
6. Retest the functionality after the fix.
7. Update the test status.

## 7. UAT Exit Criteria

UAT may be considered complete when:

* All planned test cases have been executed.
* Critical and high-priority defects have been resolved or formally accepted by the relevant stakeholders.
* Failed test cases have been retested.
* Business stakeholders have reviewed the results.
* The appropriate stakeholder has provided acceptance approval.

## 8. Expected Outcome

These UAT test cases provide a structured method for validating important e-commerce workflows and documenting whether the system meets the agreed business requirements.
