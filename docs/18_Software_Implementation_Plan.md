# 18. Software Implementation Plan

## ShopEase — E-Commerce Management System

### Document Information

| Field                  | Details                                  |
| ---------------------- | ---------------------------------------- |
| Project Name           | ShopEase E-Commerce Management System    |
| Document Type          | Software Implementation Plan             |
| Project Reference      | SE-ECOM-2026-001                         |
| Prepared By            | Vansh Patel                              |
| Project Role           | Business Analyst and Prototype Developer |
| Version                | 1.0                                      |
| Status                 | Proposed — Implementation Planning       |
| Application Type       | Web Application                          |
| Project Classification | Independent Portfolio Project            |

> **Project Context:** ShopEase is a fictional business scenario created for an independent portfolio project. The planned application will be developed and tested as a prototype. It is not a production system or an implementation delivered to a real client.

---

## 1. Purpose

This document defines the proposed technical approach for implementing
the ShopEase E-Commerce Management System.

It connects the documented business requirements to the planned
application architecture, modules, database, development activities,
and testing strategy.

The implementation will follow an iterative approach so that core
business functionality can be developed and validated before additional
features are introduced.

---

## 2. Project Objectives

The implementation aims to:

1. Provide a centralized product catalogue.
2. Allow customers to manage a shopping cart.
3. Support order creation and order tracking.
4. Provide administrators with product and order management.
5. Validate product availability during order placement.
6. Maintain consistent order and inventory records.
7. Provide basic business reporting.
8. Verify functionality through documented test cases.
9. Maintain traceability between requirements and implemented features.

These are planned objectives. Their completion will be assessed through
implementation evidence and testing.

---

## 3. Proposed Technology Stack

| Component                 | Technology            | Purpose                                            |
| ------------------------- | --------------------- | -------------------------------------------------- |
| Frontend                  | HTML5                 | Application page structure                         |
| Styling                   | CSS3                  | Layout, responsive design, and visual presentation |
| Client-side functionality | JavaScript            | Interactive interface elements                     |
| Backend                   | Python                | Business logic and request processing              |
| Web framework             | Flask                 | Application routing and backend services           |
| Database                  | SQLite                | Persistent storage for prototype data              |
| Database access           | Python `sqlite3`      | Database operations                                |
| Version control           | Git and GitHub        | Source control and project documentation           |
| Automated testing         | Python `unittest`     | Automated verification of supported functionality  |
| Manual testing            | Browser-based testing | User workflow and interface verification           |

### Technology Selection Rationale

**Flask:** Provides a lightweight framework for implementing backend
routes and business logic.

**SQLite:** Supports persistent data storage without requiring a separate
database server.

**HTML, CSS, and JavaScript:** Provide a straightforward approach to
building an interactive and responsive interface.

**Python unittest:** Allows business rules and backend operations to be
tested repeatedly.

The final technology choices may be adjusted if implementation findings
identify a better approach.

---

## 4. Proposed Application Architecture

The application will follow a simple layered architecture.

### 4.1 Presentation Layer

The presentation layer will contain the browser-based interface.

Responsibilities:

* Display product listings.
* Display product details.
* Provide shopping cart controls.
* Display checkout forms.
* Show order confirmation and status.
* Provide administrative screens.
* Display validation messages.

### 4.2 Application Layer

The application layer will be implemented using Flask and Python.

Responsibilities:

* Process HTTP requests.
* Validate submitted information.
* Apply business rules.
* Manage customer and administrator workflows.
* Calculate order totals.
* Validate product availability.
* Create and update orders.
* Return appropriate responses.

### 4.3 Data Layer

The data layer will use SQLite.

Responsibilities:

* Store product records.
* Store user and role information where authentication is implemented.
* Store order records.
* Store order items.
* Maintain inventory quantities.
* Support reporting queries.

### 4.4 Architecture Flow

```text
Customer or Administrator
            |
            v
      Web Interface
    HTML / CSS / JavaScript
            |
            v
      Flask Application
            |
            v
     Business Logic Layer
            |
            v
       SQLite Database
            |
            v
      Application Response
```

This architecture is a proposed design. The actual implementation may
evolve as development progresses.

---

## 5. Functional Modules

### 5.1 Product Catalogue

The product catalogue will allow users to view available products.

Planned capabilities:

* Display product name.
* Display description.
* Display price.
* Display available stock where appropriate.
* Display product image where available.
* Search products by name.
* Filter products by category if implemented.

### 5.2 Shopping Cart

The shopping cart will allow customers to manage selected products.

Planned capabilities:

* Add a product to the cart.
* Change product quantity.
* Remove a product.
* Calculate the subtotal.
* Validate requested quantities.
* Display an empty-cart message.

The application must validate cart contents again when an order is
submitted. Browser-side validation alone is insufficient.

### 5.3 Checkout and Order Creation

The checkout workflow will collect the information needed to create
an order.

Planned capabilities:

* Validate required checkout fields.
* Confirm product availability.
* Calculate the order total on the server.
* Create an order record.
* Create associated order-item records.
* Update inventory consistently.
* Display an order confirmation.

If order creation fails, the application should avoid leaving partially
created order records or incorrectly updated inventory.

### 5.4 Order Management

The order management module will support:

* Viewing orders.
* Viewing order items.
* Displaying order totals.
* Displaying order creation dates.
* Updating order status through authorized actions.
* Viewing order history.

The application must define which status transitions are permitted.

### 5.5 Product Administration

Authorized administrators will be able to:

* Create products.
* View products.
* Edit product details.
* Update prices.
* Update stock quantities.
* Deactivate products.

Product deletion should be handled carefully so that historical order
records remain understandable.

### 5.6 Inventory Management

Inventory functionality will support:

* Recording available stock.
* Validating stock before accepting an order.
* Reducing stock after successful order creation.
* Preventing negative inventory.
* Handling insufficient-stock requests.
* Maintaining consistency between orders and stock.

Inventory validation and updates must be performed on the server.

### 5.7 Business Reporting

A basic reporting module may display:

* Total number of orders.
* Total sales value from qualifying orders.
* Number of active products.
* Products with low stock.
* Recent orders.

The calculation rules and treatment of cancelled orders must be defined
before reporting results are considered correct.

---

## 6. User Roles and Access Control

The proposed application will distinguish between customers and
administrators.

| Capability                  | Customer | Administrator |
| --------------------------- | -------- | ------------- |
| View product catalogue      | Yes      | Yes           |
| Search products             | Yes      | Yes           |
| Manage personal cart        | Yes      | Not required  |
| Place orders                | Yes      | Not required  |
| View own orders             | Yes      | Not required  |
| View all customer orders    | No       | Yes           |
| Create products             | No       | Yes           |
| Update product records      | No       | Yes           |
| Modify inventory            | No       | Yes           |
| Update order status         | No       | Yes           |
| View administrative reports | No       | Yes           |

### Security Requirements

* Authorization must be enforced by the backend.
* Customers must not be able to access another customer's order records.
* Administrative endpoints must require administrator authorization.
* Passwords must never be stored in plaintext if authentication is implemented.
* Secrets must not be committed to the public repository.
* Inputs must be validated on the server.
* Database operations must use parameterized queries.
* Error responses must not expose sensitive application details.

These controls must be implemented and tested before claiming that the
corresponding functionality is secure.

---

## 7. Proposed Database Design

The following tables are proposed for the initial application.

### 7.1 Products

| Field          | Purpose                                    |
| -------------- | ------------------------------------------ |
| product_id     | Unique product identifier                  |
| name           | Product name                               |
| description    | Product description                        |
| price          | Product price                              |
| stock_quantity | Available inventory                        |
| category       | Product category                           |
| image_path     | Optional product image reference           |
| is_active      | Indicates whether the product is available |
| created_at     | Record creation timestamp                  |

### 7.2 Users

This table will be introduced if persistent user accounts are implemented.

| Field         | Purpose                               |
| ------------- | ------------------------------------- |
| user_id       | Unique user identifier                |
| name          | User's display name                   |
| email         | Unique account email                  |
| password_hash | Password hash, not plaintext password |
| role          | Customer or administrator             |
| created_at    | Account creation timestamp            |

### 7.3 Orders

| Field       | Purpose                   |
| ----------- | ------------------------- |
| order_id    | Unique order identifier   |
| user_id     | Reference to the customer |
| order_total | Calculated order total    |
| status      | Current order status      |
| created_at  | Order creation timestamp  |

### 7.4 Order Items

| Field         | Purpose                             |
| ------------- | ----------------------------------- |
| order_item_id | Unique order-item identifier        |
| order_id      | Reference to the order              |
| product_id    | Reference to the product            |
| product_name  | Product name snapshot at order time |
| quantity      | Ordered quantity                    |
| unit_price    | Unit price at order time            |
| line_total    | Quantity multiplied by unit price   |

Storing the product name and unit price at order time helps preserve
historical order information when product details change later.

### 7.5 Database Relationships

```text
Users
  |
  | One user can have multiple orders
  v
Orders
  |
  | One order can contain multiple items
  v
Order_Items
  |
  | Each order item references a product
  v
Products
```

Foreign keys and appropriate database constraints should be used where
supported.

Database relationships will be validated during implementation.

---

## 8. Core Business Rules

### Rule 1: Product Availability

Only active products with sufficient stock may be ordered.

### Rule 2: Quantity Validation

Order quantities must be positive integers.

### Rule 3: Price Calculation

Order totals must be calculated by the server using validated product
prices and quantities.

### Rule 4: Inventory Consistency

Stock must not become negative because of an order.

### Rule 5: Order Creation

An order and its order items must be created consistently.

### Rule 6: Order Identification

Every successfully created order must have a unique identifier.

### Rule 7: Historical Pricing

Order records should retain the applicable unit price at the time of purchase.

### Rule 8: Access Control

Only authorized users may perform administrative operations.

### Rule 9: Customer Privacy

Customers may view only the order information they are authorized to access.

### Rule 10: Order Status

Only defined and permitted status transitions may be accepted.

---

## 9. Proposed Project Structure

The initial application structure will be organized as follows:

```text
E-Commerce-System-Requirements/
|
|-- app/
|   |-- __init__.py
|   |-- routes/
|   |   |-- __init__.py
|   |   |-- products.py
|   |   |-- cart.py
|   |   |-- orders.py
|   |   |-- admin.py
|   |
|   |-- services/
|   |   |-- __init__.py
|   |   |-- product_service.py
|   |   |-- order_service.py
|   |   |-- inventory_service.py
|   |
|   |-- templates/
|   |   |-- base.html
|   |   |-- index.html
|   |   |-- products.html
|   |   |-- cart.html
|   |   |-- checkout.html
|   |   |-- order_confirmation.html
|   |   |-- order_history.html
|   |   |-- admin_dashboard.html
|   |
|   |-- static/
|   |   |-- css/
|   |   |   |-- style.css
|   |   |
|   |   |-- js/
|   |   |   |-- main.js
|
|-- database/
|   |-- schema.sql
|   |-- init_db.py
|
|-- tests/
|   |-- __init__.py
|   |-- test_products.py
|   |-- test_cart.py
|   |-- test_orders.py
|   |-- test_inventory.py
|
|-- docs/
|   |-- 01_Project_Overview.md
|   |-- ...
|   |-- 18_Software_Implementation_Plan.md
|
|-- requirements.txt
|-- run.py
|-- .gitignore
|-- README.md
```

This is the proposed structure. Files will be added as the corresponding
modules are implemented. Unnecessary files will not be created in advance.

---

## 10. Development Phases

### Phase 1: Application Setup

Activities:

* Prepare the Python environment.
* Install Flask.
* Create the application entry point.
* Establish the project folder structure.
* Confirm that the application starts successfully.

Expected evidence:

* Application starts locally.
* A basic route returns a valid response.
* Dependencies are documented.

### Phase 2: Database Setup

Activities:

* Define the database schema.
* Create the SQLite database.
* Create the required tables.
* Insert sample product records.
* Verify database operations.

Expected evidence:

* Database initialization succeeds.
* Product records can be retrieved.
* Database constraints behave as expected.

### Phase 3: Product Catalogue

Activities:

* Implement product listing.
* Implement product details.
* Add search or category filtering if included in scope.
* Create a responsive interface.

Expected evidence:

* Product information displays correctly.
* Invalid or inactive products are handled appropriately.

### Phase 4: Shopping Cart

Activities:

* Add cart items.
* Update quantities.
* Remove items.
* Calculate subtotals.
* Validate quantities.

Expected evidence:

* Cart operations work as specified.
* Invalid quantities are rejected.
* Totals are calculated correctly.

### Phase 5: Order Processing

Activities:

* Implement checkout.
* Validate order data.
* Verify stock availability.
* Create orders and order items.
* Update inventory consistently.
* Display order confirmation.

Expected evidence:

* Valid orders are created.
* Invalid orders are rejected.
* Inventory remains consistent.

### Phase 6: Administration

Activities:

* Implement product management.
* Implement inventory updates.
* Implement order management.
* Apply authorization controls.

Expected evidence:

* Authorized administrative operations succeed.
* Unauthorized operations are rejected.

### Phase 7: Testing

Activities:

* Execute functional tests.
* Execute negative tests.
* Test inventory boundary conditions.
* Test authorization.
* Record actual results.
* Document defects and retest fixes.

Expected evidence:

* Test execution records.
* Defect log.
* Requirements traceability updates.

### Phase 8: Project Review

Activities:

* Review scope and requirements coverage.
* Document implemented functionality.
* Capture application screenshots.
* Summarize test outcomes.
* Record limitations and future improvements.
* Update the GitHub README.

Expected evidence:

* Final project report.
* Demonstration screenshots.
* Accurate implementation and testing status.

---

## 11. Testing Strategy

Testing will be based on the documented requirements and acceptance criteria.

### Functional Testing

Verify that each supported feature behaves as expected.

### Negative Testing

Verify that invalid input, insufficient stock, and unauthorized
operations are handled appropriately.

### Boundary Testing

Test quantities and values at their permitted limits.

### Integration Testing

Verify interactions between the cart, order processing, inventory,
and database.

### Regression Testing

Repeat relevant tests after defects are fixed or functionality changes.

### User Acceptance Testing

Evaluate whether the implemented workflows satisfy the documented
acceptance criteria.

The existing UAT test cases will be reviewed and mapped to implemented
features before execution.

A test case must not be marked as Passed until its actual result has
been observed and recorded.

---

## 12. Definition of Done

A feature will be considered complete when:

1. Its requirement is documented.
2. Its expected behavior is defined.
3. Its implementation is completed.
4. Input validation is implemented where required.
5. Relevant tests have been executed.
6. Test results have been recorded.
7. Identified defects have been addressed or documented.
8. Related project documentation is updated.

A feature that has only been designed or documented will remain marked
as Planned or In Progress.

---

## 13. Key Risks and Mitigation

| Risk                    | Potential Impact             | Proposed Mitigation                               |
| ----------------------- | ---------------------------- | ------------------------------------------------- |
| Incomplete requirements | Missing functionality        | Review requirements before implementation         |
| Incorrect order totals  | Financial calculation errors | Test calculation rules and edge cases             |
| Inventory inconsistency | Incorrect stock records      | Use transactions and validate stock on the server |
| Unauthorized access     | Improper data access         | Enforce backend authorization                     |
| Database errors         | Failed operations            | Validate constraints and handle exceptions        |
| Insufficient testing    | Undetected defects           | Maintain test coverage and execution records      |
| Scope expansion         | Delayed delivery             | Prioritize features and document changes          |

---

## 14. Proposed Future Improvements

Potential future improvements include:

* Real authentication and password reset.
* Payment gateway integration in an appropriately secured environment.
* Email order notifications.
* Product reviews.
* Advanced search and filtering.
* Sales analytics dashboard.
* Exportable business reports.
* Deployment to a hosting platform.
* Additional automated integration tests.

These features will be considered only after the core prototype is
implemented and evaluated.

---

## 15. Implementation Status

| Component                         | Current Status         |
| --------------------------------- | ---------------------- |
| Business Case and Project Charter | Documented             |
| Client Project Brief              | Documented             |
| Business Analysis Documentation   | Prepared               |
| Technical Implementation Plan     | Documented             |
| Application Environment           | Not yet verified       |
| Database Implementation           | Pending                |
| Product Catalogue                 | Pending                |
| Shopping Cart                     | Pending                |
| Order Processing                  | Pending                |
| Administration Module             | Pending                |
| Automated Testing                 | Pending implementation |
| Final Demonstration               | Pending                |

The status table must be updated as implementation progresses.

---

## 16. Conclusion

This implementation plan establishes the proposed architecture,
technical stack, functional modules, database structure, business rules,
development phases, and testing strategy for the ShopEase prototype.

The next activity is to prepare the local development environment and
create the initial Flask application.

Subsequent features will be implemented incrementally and verified
against the requirements documented in this repository.

---

**Document Status:** Proposed — Implementation Planning

**Version:** 1.0

**Prepared By:** Vansh Patel
