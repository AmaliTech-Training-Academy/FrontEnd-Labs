# Test Management with Excel

## Project Objectives

- Develop a comprehensive test plan aligned with project goals and stakeholder expectations, covering scope, objectives, and resources.  

- Develop detailed test case documentation that covers both functional and non-functional requirements, ensuring thorough test coverage and clear, reproducible testing steps, including a Requirement Traceability Matrix (RTM).  

- Utilize Microsoft Excel as a test management tool.  

- Manage defects using Excel to log, prioritize, and track bugs.  

---

## Project Overview

**The Product Store** is an e-commerce platform designed to provide customers with a seamless online shopping experience. Customers can browse and purchase a variety of products available on the website.

### Key Features

- **Product Browsing:**  
  Customers can explore a wide range of products with detailed descriptions, prices, and images.  

- **Shopping Cart:**  
  Customers can add products to their cart, review selections, and prepare for checkout.  

- **Order Placement:**  
  Customers can complete purchases through a secure order process.  

---

## User Stories

### User Story 1: Homepage

**As a Customer**, I want to visit the homepage so that I can access and browse available products.

#### Acceptance Criteria

1. The homepage should load quickly and be accessible without login.  
2. The homepage should have a clear layout with navigation options (Home, Contact, Cart, Login).  
3. Each product should display:
   - Product name  
   - Price  
   - Thumbnail image  
4. Clicking a product name should redirect to a detailed product page with:
   - Full description  
   - Price  
   - Images  
   - "Add to Cart" button  

---

### User Story 2: Cart

**As a Customer**, I want to manage items in my cart so that I can prepare for checkout.

#### Acceptance Criteria

1. Customers should be able to add products using the "Add to Cart" button.  
2. The system should provide immediate feedback (e.g., "Product added to cart").  
3. The cart should display total cost dynamically.  
4. Customers should be able to:
   - Add the same product multiple times (increase quantity)  
   - Delete products from the cart  
5. Cart updates should reflect immediately after changes.  
6. The cart page should include a **"Place Order"** button.  

---

### User Story 3: Place an Order

**As a Customer**, I want to place an order so that I can complete my purchase.

#### Acceptance Criteria

1. Customers should be able to click the "Place Order" button.  
2. The button should only be enabled when the cart is not empty.  
3. A form should be displayed upon clicking the button.  

#### Form Requirements

- **Name (Required):**  
  - Accept only alphabetic characters  

- **Credit Card Information (Required):**  
  - Accept only numeric input  
  - Must be 16 digits  

- **Optional Fields:**  
  - Shipping address  
  - Phone number  
  - Special instructions  

4. Credit card data must be securely processed (not stored in plain text).  
5. Successful submission should display an order confirmation page.  

---

## Grading Scheme

### 1. Test Plan Document

| Metric                                      | Score |
|---------------------------------------------|-------|
| Comprehensive Test Plan                     | 15    |

---

### 2. Test Case Development

| Field                | Description                          |
|---------------------|--------------------------------------|
| Test Case ID        | Unique identifier                    |
| Test Scenario       | High-level scenario                  |
| Test Case           | Detailed test description            |
| Test Data           | Input data                           |
| Test Execution Steps| Steps to execute                     |
| Expected Results    | Expected outcome                     |
| Actual Results      | Actual outcome after execution       |
| Status (Pass/Fail)  | Test result                          |

**Score:** 50  

---

### 3. Requirement Traceability Matrix (RTM)

| Field                     | Description                         |
|--------------------------|-------------------------------------|
| Requirement ID           | Unique requirement identifier       |
| Description              | Requirement details                 |
| Requirement Source       | Origin of requirement               |
| Test Case ID             | Linked test case                    |
| Test Case Description    | Summary of test case                |
| Test Status              | Pass/Fail                           |
| Defect ID                | Linked defect (if applicable)       |

**Score:** 15  

---

### 4. Defect Management

| Field                | Description                          |
|---------------------|--------------------------------------|
| Bug ID              | Unique identifier                    |
| Bug Description     | Description of the issue             |
| Steps to Reproduce  | Steps to recreate the bug            |
| Expected Results    | Expected outcome                     |
| Actual Results      | Actual outcome                       |
| Environment         | Testing environment                  |
| Severity            | Impact level                         |
| Priority            | Urgency level                        |
| Status              | Current state of bug                 |
| Assignee            | Responsible person                   |

**Score:** 20  

---

## Total Score

**100 Marks**

---

## Notes

- All test management activities should be conducted using Microsoft Excel.  
- Ensure proper organization of sheets:
  - Test Plan  
  - Test Cases  
  - RTM  
  - Defect Log  
- Maintain consistency in naming conventions and IDs across all documents.  
