# E-Commerce System — Acceptance Criteria

## 1. Purpose

This document defines the acceptance criteria for selected user stories in the E-Commerce System. These criteria help the development and testing teams determine whether each feature meets the agreed requirements.

## 2. US-01: Customer Registration

**User Story:** As a customer, I want to register an account so that I can access the e-commerce system.

### Acceptance Criteria

* **AC-01:** The system shall allow customers to submit all required registration fields.
* **AC-02:** The system shall display validation messages when mandatory fields are missing or invalid.
* **AC-03:** The system shall create an account when all required details are valid and the registration succeeds.
* **AC-04:** The system shall inform the customer if the email address is already registered.

## 3. US-02: Customer Login

**User Story:** As a registered customer, I want to log in securely so that I can access my account.

### Acceptance Criteria

* **AC-05:** The system shall allow login using valid credentials.
* **AC-06:** The system shall display an appropriate error message when credentials are invalid.
* **AC-07:** The system shall prevent unauthorized access to protected account pages.
* **AC-08:** The system shall provide a secure logout option.

## 4. US-03: Product Search

**User Story:** As a customer, I want to search for products so that I can find items quickly.

### Acceptance Criteria

* **AC-09:** The system shall allow customers to enter a product name or keyword.
* **AC-10:** The system shall display products matching the search criteria.
* **AC-11:** The system shall display an appropriate message when no matching products are found.

## 5. US-05: Add Product to Cart

**User Story:** As a customer, I want to add products to my shopping cart so that I can purchase selected items.

### Acceptance Criteria

* **AC-12:** The system shall allow customers to add available products to the cart.
* **AC-13:** The system shall display the selected product and quantity in the cart.
* **AC-14:** The system shall prevent adding quantities that exceed available stock.
* **AC-15:** The system shall update the cart total when items are added or quantities change.

## 6. US-07: Review Order Total

**User Story:** As a customer, I want to review my order total before checkout so that I understand the amount payable.

### Acceptance Criteria

* **AC-16:** The system shall display the selected products and quantities.
* **AC-17:** The system shall calculate the subtotal correctly.
* **AC-18:** The system shall display applicable taxes, delivery charges, and discounts where configured.
* **AC-19:** The system shall display the final payable amount before the customer confirms payment.

## 7. US-09: Online Payment

**User Story:** As a customer, I want to pay using an available payment method so that I can complete my purchase.

### Acceptance Criteria

* **AC-20:** The system shall submit the payment request to the configured payment provider.
* **AC-21:** The system shall confirm payment only after receiving a valid success response.
* **AC-22:** The system shall display an appropriate message when payment fails.
* **AC-23:** The system shall allow the customer to retry a failed payment where supported.
* **AC-24:** The system shall prevent duplicate order creation when payment requests are repeated.

## 8. US-10: Order Confirmation

**User Story:** As a customer, I want to receive an order confirmation so that I know my order has been placed.

### Acceptance Criteria

* **AC-25:** The system shall generate a unique order ID for a successfully placed order.
* **AC-26:** The system shall display the order ID and order summary.
* **AC-27:** The system shall display the appropriate payment status.
* **AC-28:** The system shall not incorrectly mark an unsuccessful payment as completed.

## 9. US-11: Order Tracking

**User Story:** As a customer, I want to track my order so that I can check its current status.

### Acceptance Criteria

* **AC-29:** The system shall display orders belonging to the authenticated customer.
* **AC-30:** The system shall display the latest available status for each order.
* **AC-31:** The system shall prevent customers from accessing another customer's order information.

## 10. US-13: Admin Product Management

**User Story:** As an administrator, I want to add and update products so that customers see accurate product information.

### Acceptance Criteria

* **AC-32:** The system shall allow authorized administrators to add products with valid required information.
* **AC-33:** The system shall allow authorized administrators to update product details.
* **AC-34:** The system shall validate required product fields before saving changes.
* **AC-35:** The system shall prevent unauthorized users from accessing product administration features.

## 11. Definition of Acceptance

A user story can be considered accepted when:

* Its acceptance criteria have been reviewed.
* The required behavior has been tested.
* No unresolved critical defects prevent acceptance.
* The agreed business requirements are satisfied.
* The appropriate stakeholder or authorized representative approves the result.

## 12. Conclusion

Acceptance criteria establish clear expectations for system behavior. They help developers understand requirements, guide testers in validating features, and support User Acceptance Testing (UAT).
