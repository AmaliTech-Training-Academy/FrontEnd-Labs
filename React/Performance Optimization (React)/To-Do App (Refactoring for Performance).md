# React Performance Optimization: To Do App

## Learning Objectives

By the end of this module, you should be able to:

- Identify and resolve common performance bottlenecks in React applications.  
- Optimize rendering using React.memo, useCallback, and useMemo to prevent unnecessary component re-renders.  
- Implement code-splitting using React.lazy and Suspense for improved load times.  
- Use list virtualization (e.g., react-window or react-virtualized) to efficiently render large lists.  
- Manage expensive computations and derived state efficiently using memoization and custom hooks.  
- Apply best practices for improving perceived performance and responsiveness in production-ready React applications.  

---

## Introduction

In this lab, you will take the provided legacy React To-Do application and refactor it to meet modern React performance and architectural standards. The existing code contains several anti-patterns that cause inefficient re-renders, unnecessary computations, and poor scalability. Your goal is to transform the application into a high-performance, maintainable, and production ready React application.

### Get the project setup from :  [GitHub - Dacostasolo/learner-code-optimization](https://github.com/Dacostasolo/learner-code-optimization)
---

## Lab Requirements

- Node.js (v18 or later)  
- React (v18 or later, with Vite or CRA setup)  
- The provided legacy-todo-app.js code  
- Code Editor (VS Code recommended)  

**Estimated Duration:** 4–5 hours (Hands-on Practice & Implementation)

---

## Lab Tasks

### Task 1: Baseline Diagnosis and App Setup

**Initial Setup:**  
Create a new React application (Vite or Create React App) and integrate the provided legacy-todo-app.js code into the main component.  

**Performance Baseline:**  
Use the React DevTools Profiler to capture the initial render and identify unnecessary re-renders when interacting with the app.  

**Architectural Review:**  
Document observed anti-patterns such as prop drilling, inline function recreation, and lack of memoization.  

---

### Task 2: Rendering Optimization and State Refactor

**Apply React.memo:**  
Wrap presentational components with React.memo to prevent needless re-renders.  

**Optimize Handlers:**  
Use useCallback to memoize event handlers and avoid re-creation on every render.  

**Derived State:**  
Use useMemo to cache computed values like completed task counts or filtered todos.  

**State Refactor:**  
Move global or shared state to a custom hook or context provider (useTodos or TodoProvider) to improve maintainability and reduce prop drilling.  

---

### Task 3: Code-Splitting and Security Enhancements

**Code Splitting:**  
Implement React.lazy and Suspense for lazy-loading routes or large components (e.g., TodoList, StatsPanel).  

**Virtualization:**  
Integrate a list virtualization library (react-window) to optimize large task lists.  

**Input Sanitization:**  
Identify XSS vulnerabilities from rendering raw user input and fix them using libraries like DOMPurify before rendering HTML content.  

---

### Task 4: Modularity and Component Reusability

**Refactor Components:**  
Split the monolithic To-Do component into smaller, reusable components (e.g., TodoItem, TodoInput, TodoList, TodoStats).  

**Improve File Structure:**  
Adopt a feature-based folder organization (e.g., /components, /hooks, /context, /utils).  

**Ensure Testability:**  
Use mock state and props to test re-render behavior in isolation.  

---

## Assessment Criteria

| Criteria                                             | Weight |
|-----------------------------------------------------|--------|
| Rendering Optimization (React.memo, useMemo, useCallback) | 30%   |
| Architectural Refactor (Hooks & Context)            | 30%   |
| Code-Splitting & Virtualization                     | 20%   |
| Security & Input Handling                           | 10%   |
| Code Quality & Modularity                           | 10%   |

---

## Lab Deliverables

- Updated To-Do App Codebase showing measurable performance improvement.  
- Before/After Profiling Screenshots from React DevTools highlighting reduced re-render counts and commit times.  
- GitHub Repository with clear commit messages reflecting each refactor step.  
- Final Folder Structure demonstrating modular, maintainable architecture with React best practices.
