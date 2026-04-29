# Automation Test Execution with Jenkins CI/CD

## Project Overview

This project seeks to help QA engineers have hands-on practice to set up a Jenkins pipeline to automatically trigger and execute tests upon code commits or scheduled builds. It simulates a real-world CI/CD setup where Jenkins pulls the latest test automation code from a Git repository, builds the project (if applicable), runs the test suite, and generates reports.

## Objectives

Understand how CI/CD supports test automation  

Learn how to create Jenkins jobs or pipelines for testing  

Automate code pulls, test execution, and reporting in Jenkins  

Integrate reports and basic alerting in Jenkins  

## Tasks

A working test suite  

API tests here using REST Assured  

Host code in a GitHub repo:  

Code should include a README.md, test files, and a Dockerfile  

Set up Jenkins:  

Install Jenkins locally or run via Docker (jenkins/jenkins:lts)  

Install required Jenkins plugins (e.g., Git, Pipeline, HTML publisher, JUnit, etc.)  

Configure a Jenkins Pipeline Job:  

Pull code from the repo  

Build and install dependencies  

Run tests automatically  

Archive and publish test reports  

Webhook and notification:  

Add webhook to trigger job on push  

Add Slack/email notifications  

Use Jenkinsfile (declarative or scripted)  

## Grading Scheme

METRIC | SCORE | Total
--- | --- | ---
Test suite scripts | 20 | 
Jenkins setup | 25 | 
Jenkins pipeline | 40 | 
Notifications | 15 | 
Lab submission |  | 100
