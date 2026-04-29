# Test Management with Jira - Xray

## Project Objectives

- Develop a comprehensive test plan aligned with project goals and stakeholder expectations, covering scope, objectives, and resources.  

- Develop detailed test case documentation that covers both functional and non-functional requirements, ensuring thorough test coverage and clear, reproducible testing steps.  

- Utilize Jira with Xray for test management.  

- Manage defects using Jira Xray to log, prioritize, and track bugs.  

---

## Project Overview

The **XYZ Bank App** is a digital banking platform designed for two primary user groups: **Customers** and **Bank Managers**.

### For Customers
The application provides essential banking functionalities, including:
- Secure login  
- Deposit funds  
- Withdraw money  
- Access account-related services  

### For Bank Managers
The application provides administrative capabilities, including:
- Adding new customers  
- Creating accounts  
- Deleting accounts  

---

## Requirements

- Develop a test plan for the project  
- Perform manual testing on the application  
- Manage testing activities using Jira - Xray  
- Access and test the application via: **XYZ Bank App**  

---

## User Stories

### User Story 1: Bank Manager

**As a Bank Manager**, I want to manage customer accounts efficiently by adding customers, creating accounts, and deleting accounts.

#### Acceptance Criteria

**Adding Customers**
- The system should allow managers to add new customers  
- Customer names must contain only alphabetic characters  
- Postal codes must contain only numeric characters  

**Creating Accounts**
- Managers should be able to create accounts for existing customers  
- Customers cannot access accounts until they are created  

**Deleting Accounts**
- Managers should be able to delete customer accounts  
- Deleted accounts should no longer be accessible by customers  

---

### User Story 2: Customer

**As a Customer**, I want to manage my finances by viewing transactions, depositing funds, and withdrawing money.

#### Acceptance Criteria

**Viewing Transactions**
- Customers should be able to view recent transaction history  

**Depositing Funds**
- Customers should be able to enter a deposit amount  
- Deposit must be validated (positive value)  
- Account balance should update after successful deposit  

**Withdrawing Money**
- Customers should be able to enter withdrawal amount  
- Withdrawal must be validated:
  - Positive value  
  - Sufficient balance  
- Account balance should update after successful withdrawal  

**Transaction Security**
- Customers should not be able to alter or reset transaction history  

---

## Grading Scheme

### 1. Test Plan Document

| Metric              | Score |
|---------------------|-------|
| Test Plan Document  | 15    |

---

### 2. Test Case Development

- Use **Jira Xray** to:
  - Create test cases  
  - Link test cases to requirements  
  - Organize test executions  

**Score:** 50  

---

### 3. Requirement Traceability Matrix (RTM)

- Generate RTM using **Jira Xray**
- Ensure:
  - Requirements are linked to test cases  
  - Test execution status is visible  

**Score:** 15  

---

### 4. Defect Management

- Use **Jira Xray** to:
  - Log bugs as issues  
  - Assign severity and priority  
  - Link defects to test cases  

**Score:** 20  

---

## Total Score

**100 Marks**

---

## Notes

- Ensure proper usage of Jira Xray features:
  - Test Repository  
  - Test Sets  
  - Test Plans  
  - Test Executions  

- Maintain clear traceability between:
  - Requirements  
  - Test Cases  
  - Defects  

- Follow consistent naming conventions for:
  - Test Cases (e.g., TC_001)  
  - Bugs (e.g., BUG_001)  
  - Requirements (e.g., REQ_001)  

- Keep all test artifacts updated throughout the testing lifecycle.  
