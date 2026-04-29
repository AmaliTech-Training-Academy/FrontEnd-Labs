# React Testing: Kanban App
## Learning Objectives

By the end of this lab, you should be able to:

- Write and organize unit tests for React components using Jest or Vitest.
- Test state-driven logic and UI rendering in isolation.
- Mock API calls and verify correct handling of loading and error states.
- Maintain a scalable and consistent testing structure across the Kanban app.

## Introduction

In this lab, you'll extend your Kanban Task Management App by introducing **automated testing**.

Testing ensures your app's components, global state, and data flows remain reliable as the project grows.

You'll create focused tests that validate user interactions, data fetching, and state updates — helping to prevent regressions as new features are introduced.

By the end of this lab, your Kanban app should have a foundational test suite that runs consistently and verifies the most critical user flows.

## Tasks

### Task 1: Configure the Testing Environment

Set up **Jest** or **Vitest** in your project (depending on your setup).

Ensure your testing framework supports React Testing Library for component testing.

Add configuration scripts for running tests and watching changes.

### Task 2: Write Unit Tests for Core Components

Select key UI components — such as the **TaskCard**, **Board**, or **Column** components.

Write tests that verify component rendering based on given props or store data.

Check that text content, buttons, and other UI elements appear as expected.

### Task 3: Mock API Calls

Mock API calls used in data fetching.

Test how your components handle loading, success, and error responses.

Verify that the correct UI feedback (loading spinner, error message, etc.) appears under each condition.

### Task 4: Simulate User Interactions

Use React Testing Library's event simulation utilities to mimic user actions like:
- Adding a new task
- Editing or deleting a task
- Navigating between boards

Ensure that the UI and state update accurately after each interaction.

### Task 5: Maintain Testing Coverage and Structure

Organize your test files consistently.

Run coverage reports and identify untested areas.

Document your testing structure in the README to guide future contributors.

## Evaluation Criteria

| Criteria | Description | Weight |
|---|---|---|
| Environment Setup | Testing framework and tools are correctly configured | 15% |
| Component Tests | Components render and behave correctly under test | 25% |
| State Tests | Global state updates and actions are validated | 20% |
| API & Async Tests | API calls are properly mocked and handled in tests | 25% |
| Code Quality & Coverage | Tests are organized, readable, and maintainable | 15% |

---

# React Performance Lab — To-Do App (Refactoring for Performance)

## Overview

In this lab, you will take the provided legacy React To-Do application and refactor it to meet modern React performance and architectural standards. The existing code contains several anti-patterns that cause inefficient re-renders, unnecessary computations, and poor scalability. Your goal is to transform the application into a high-performance, maintainable, and production-ready React application.

Get the project setup from: [GitHub - Dacostasolo/learner-code-optimization](https://github.com/Dacostasolo/learner-code-optimization)

## Learning Objectives

By the end of this module, you should be able to:

- Identify and resolve common performance bottlenecks in React applications.
- Optimize rendering using **React.memo**, **useCallback**, and **useMemo** to prevent unnecessary component re-renders.
- Implement **code-splitting** using **React.lazy** and **Suspense** for improved load times.
- Use **list virtualization** (e.g., react-window or react-virtualized) to efficiently render large lists.
- Manage expensive computations and derived state efficiently using **memoization** and **custom hooks**.
- Apply best practices for improving **perceived performance** and responsiveness in production-ready React applications.

## Lab Requirements

- Node.js (v18 or later)
- React (v18 or later, with Vite or CRA setup)
- The provided legacy-todo-app.js code
- Code Editor (VS Code recommended)

**Estimated Duration:** 4–5 hours

## Lab Tasks

### Task 1: Baseline Diagnosis and App Setup

- **Initial Setup:** Create a new React application (Vite or Create React App) and integrate the provided legacy-todo-app.js code into the main component.
- **Performance Baseline:** Use the React DevTools Profiler to capture the initial render and identify unnecessary re-renders when interacting with the app.
- **Architectural Review:** Document observed anti-patterns such as prop drilling, inline function recreation, and lack of memoization.

### Task 2: Rendering Optimization and State Refactor

- **Apply React.memo:** Wrap presentational components with React.memo to prevent needless re-renders.
- **Optimize Handlers:** Use useCallback to memoize event handlers and avoid re-creation on every render.
- **Derived State:** Use useMemo to cache computed values like completed task counts or filtered todos.
- **State Refactor:** Move global or shared state to a custom hook or context provider (useTodos or TodoProvider) to improve maintainability and reduce prop drilling.

### Task 3: Code-Splitting and Security Enhancements

- **Code Splitting:** Implement **React.lazy** and **Suspense** for lazy-loading routes or large components (e.g., TodoList, StatsPanel).
- **Virtualization:** Integrate a list virtualization library (react-window) to optimize large task lists.
- **Input Sanitization:** Identify XSS vulnerabilities from rendering raw user input and fix them using libraries like DOMPurify before rendering HTML content.

### Task 4: Modularity and Component Reusability

- **Refactor Components:** Split the monolithic To-Do component into smaller, reusable components (e.g., TodoItem, TodoInput, TodoList, TodoStats).
- **Improve File Structure:** Adopt a feature-based folder organization (e.g., /components, /hooks, /context, /utils).
- **Ensure Testability:** Use mock state and props to test re-render behavior in isolation.

## Assessment Criteria

| Criteria | Weight |
|---|---|
| Rendering Optimization (React.memo, useMemo, useCallback) | 30% |
| Architectural Refactor (Hooks & Context) | 30% |
| Code-Splitting & Virtualization | 20% |
| Security & Input Handling | 10% |
| Code Quality & Modularity | 10% |

## Lab Deliverables

- **Updated To-Do App Codebase** showing measurable performance improvement.
- **Before/After Profiling Screenshots** from React DevTools highlighting reduced re-render counts and commit times.
- **GitHub Repository** with clear commit messages reflecting each refactor step.
- **Final Folder Structure** demonstrating modular, maintainable architecture with React best practices.
