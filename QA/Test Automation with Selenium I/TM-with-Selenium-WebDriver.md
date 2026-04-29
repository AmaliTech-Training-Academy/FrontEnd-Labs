# Test Automation with Selenium WebDriver

## Project Objectives

Set Up Selenium WebDriver:  

Learn how to install and configure Selenium WebDriver with ChromeDriver for automated browser testing.  

Implement JUnit 5/TestNG for Test Execution:  

Use JUnit 5 or TestNG annotations to structure test cases effectively.  

Automate a Simple Web Test – Write and execute a basic UI test.  

Set up a Continuous Integration (CI) pipeline using GitHub Actions to automate Selenium tests.  

---

## PROJECT Description: Selenium WebDriver Setup and Basic UI Testing

---

## Overview

Setup and configuration  

Maven / Gradle  

Add Selenium WebDriver and JUnit 5 / TestNG dependencies in the pom.xml  

---

## Basic Automated Test

Launch the Newsletter sign-up form with success message project using Selenium and ChromeDriver  

---

## Implement Page Object Model (POM)

- Create separate Page Classes for each page  
- Use locators to identify elements  
- Implement a Page Factory Pattern for better test structure  

---

## CI Pipeline (GitHub Actions)

- Create a `.github/workflows/ci.yml` configuration for GitHub Actions  
- Ensure the workflow is triggered on code push or pull request events  
- Set up the CI pipeline to automatically install dependencies and run the tests using GitHub Actions  
- Set up notifications (email or Slack) to notify team of build status (pass/fail)  
- Ensure GitHub Actions logs include detailed information on test execution  

---

## Grading Scheme

| METRIC | SCORE | TOTAL |
|--------|-------|-------|
| Setup and configuration | 15 | |
| Basic Automated Test using JUnit 5/TestNG | 35 | |
| Page Object Model (POM) | 20 | |
| GitHub Actions | 30 | |
| **TOTAL** | | **100** |
