# Functional Requirements Document (FRD)

## 1. Purpose

This document defines the functional requirements of the E-Commerce System. It describes the system features and behaviors required to support customer shopping activities and administrative operations.

## 2. Customer Registration and Login

| Requirement ID | Functional Requirement                                                                    | Priority |
| -------------- | ----------------------------------------------------------------------------------------- | -------- |
| FR-01          | The system shall allow new customers to register using the required information.          | High     |
| FR-02          | The system shall validate mandatory registration fields.                                  | High     |
| FR-03          | The system shall allow registered customers to log in using valid credentials.            | High     |
| FR-04          | The system shall display an appropriate error message when login credentials are invalid. | High     |

## 3. Product Search and Browsing

| Requirement ID | Functional Requirement                                                                   | Priority |
| -------------- | ---------------------------------------------------------------------------------------- | -------- |
| FR-05          | The system shall display available products to customers.                                | High     |
| FR-06          | The system shall allow customers to search for products by name or keyword.              | High     |
| FR-07          | The system shall display product name, price, description, and availability.             | High     |
| FR-08          | The system shall prevent customers from ordering quantities that exceed available stock. | High     |

## 4. Shopping Cart

| Requirement ID | Functional Requirement                                                             | Priority |
| -------------- | ---------------------------------------------------------------------------------- | -------- |
| FR-09          | The system shall allow customers to add available products to their shopping cart. | High     |
| FR-10          | The system shall allow customers to remove products from their cart.               | High     |
| FR-11          | The system shall allow customers to update product quantities.                     | High     |
| FR-12          | The system shall calculate and display the cart subtotal.                          | High     |

## 5. Checkout and Payment

| Requirement ID | Functional Requirement                                                                                    | Priority |
| -------------- | --------------------------------------------------------------------------------------------------------- | -------- |
| FR-13          | The system shall allow customers to proceed to checkout when their cart contains valid items.             | High     |
| FR-14          | The system shall allow customers to enter or confirm delivery details.                                    | High     |
| FR-15          | The system shall display the order summary and final payable amount before payment.                       | High     |
| FR-16          | The system shall submit payment requests to the configured external payment provider.                     | High     |
| FR-17          | The system shall display payment success or failure information based on the payment provider's response. | High     |

## 6. Order Management and Tracking

| Requirement ID | Functional Requirement                                                                                              | Priority |
| -------------- | ------------------------------------------------------------------------------------------------------------------- | -------- |
| FR-18          | The system shall create an order after the order is successfully confirmed according to the payment method's rules. | High     |
| FR-19          | The system shall generate a unique order identifier for each order.                                                 | High     |
| FR-20          | The system shall display order confirmation and order details to the customer.                                      | High     |
| FR-21          | The system shall allow customers to view their order history.                                                       | Medium   |
| FR-22          | The system shall display the latest available status of each order.                                                 | High     |
| FR-23          | The system shall allow customers to cancel orders that meet the defined cancellation rules.                         | Medium   |

## 7. Admin Product Management

| Requirement ID | Functional Requirement                                                               | Priority |
| -------------- | ------------------------------------------------------------------------------------ | -------- |
| FR-24          | The system shall allow authorized administrators to add products.                    | High     |
| FR-25          | The system shall allow authorized administrators to update product information.      | High     |
| FR-26          | The system shall allow authorized administrators to deactivate products.             | Medium   |
| FR-27          | The system shall allow authorized administrators to update product stock quantities. | High     |

## 8. Admin Order Management and Reporting

| Requirement ID | Functional Requirement                                                                                     | Priority |
| -------------- | ---------------------------------------------------------------------------------------------------------- | -------- |
| FR-28          | The system shall allow authorized administrators to view customer orders.                                  | High     |
| FR-29          | The system shall allow authorized administrators to update order status according to the defined workflow. | High     |
| FR-30          | The system shall provide basic sales and order reports to authorized administrators.                       | Medium   |

## 9. Requirement Validation

Each functional requirement should be reviewed for clarity, consistency, feasibility, and testability.

The requirements should be linked to their corresponding business requirements and UAT test scenarios to support requirement traceability.

## 10. Conclusion

These functional requirements describe the expected behavior of the E-Commerce System and provide a foundation for user stories, acceptance criteria, development activities, and UAT.
