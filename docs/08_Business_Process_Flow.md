# Business Process Flow

## 1. Purpose

This document describes the main business process flow for an e-commerce system, from customer registration to successful order placement and order tracking.

## 2. Customer Order Process

### Process Flow

1. Customer opens the e-commerce website.
2. Customer registers or logs in.
3. Customer searches for or browses products.
4. Customer selects a product.
5. System displays product details, price, and availability.
6. Customer adds the product to the shopping cart.
7. Customer reviews the cart and order total.
8. Customer proceeds to checkout.
9. Customer enters or confirms the delivery address.
10. System validates the order details.
11. Customer selects a payment method.
12. Payment gateway processes the payment.
13. System checks the payment result.
14. If payment is successful, the system creates the order and displays an order confirmation.
15. If payment fails, the system informs the customer and allows another payment attempt.
16. Customer views the order status through the order tracking feature.

## 3. Business Process Diagram

```text
        Start
          |
          v
   Open E-Commerce Website
          |
          v
   Register / Log In
          |
          v
   Search or Browse Products
          |
          v
     Select a Product
          |
          v
   Add Product to Cart
          |
          v
    Review Shopping Cart
          |
          v
        Checkout
          |
          v
   Confirm Delivery Address
          |
          v
    Select Payment Method
          |
          v
    Process Payment
          |
          v
    Payment Successful?
       /          \
     Yes           No
      |             |
      v             v
 Create Order   Display Payment
      |          Failure Message
      v             |
 Show Order         v
 Confirmation   Retry Payment
      |
      v
 Track Order
      |
      v
      End
```

## 4. Business Rules

* Customers must provide valid information to register an account.
* Customers must provide the required checkout details before placing an order.
* The system must calculate the order total before payment.
* An order must not be marked as successfully paid unless payment confirmation is received.
* Customers must receive an order confirmation after successful order placement.
* Customers must be able to view the status of their orders.
* Payment failures must be communicated clearly to customers.

## 5. Exception Handling

| Scenario                     | Expected System Response                                               |
| ---------------------------- | ---------------------------------------------------------------------- |
| Invalid login details        | Display an error message and allow another attempt.                    |
| Product unavailable          | Inform the customer that the product is unavailable.                   |
| Invalid delivery information | Ask the customer to correct the information.                           |
| Payment failure              | Display a failure message and allow a retry.                           |
| Order confirmation issue     | Display an appropriate message and retain the order status accurately. |

## 6. Business Analyst Contribution

The Business Analyst documents the existing and proposed process, identifies decision points and exceptions, clarifies business rules, and ensures that stakeholders agree on the expected system behaviour.

## 7. Expected Outcome

The documented process provides a shared understanding of the customer order journey and helps the development and testing teams implement and validate the required functionality.
