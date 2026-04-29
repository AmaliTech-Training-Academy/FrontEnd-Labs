## Learning Objectives

By the end of this lab, you should be able to:

- Create a **global state layer** using the Context API.
- Manage complex state updates with **useReducer**.
- Eliminate prop drilling by accessing shared state from any component.
- Ensure predictable state transitions through a centralized reducer.
- Maintain clean, modular, and testable application architecture.

## Introduction

In this lab, you'll extend your Kanban project to make your state **global** and **centrally managed** using React's **Context API** and **useReducer**.

Your goal is to transition from local state management within components to a single, organized global store that handles all board and task interactions.

## Project Overview

Continue working on your **Kanban Board Project**.

Your task is to refactor it so that the entire application — boards, columns, and tasks — operates on a shared global state accessible from anywhere in the app.

You'll also introduce a **reducer function** that defines all possible actions (e.g., adding, moving, and deleting tasks) to ensure that updates remain predictable and easy to maintain.

## Tasks

### Task 1: Establish a Global Context

Define a new global context responsible for managing the overall board and task data.

All components that depend on shared information should consume this context rather than passing props down the tree.

### Task 2: Introduce a Reducer for State Transitions

Use a reducer to describe how the global state should change in response to specific actions.

Each state transition should be clearly defined by an action type and payload.

### Task 3: Replace Local State with Global State

Refactor existing components to rely on the shared global context instead of internal useState hooks.

Ensure that state updates flow through the reducer consistently.

### Task 4: Synchronize State Across Routes

Ensure that navigating between routes (e.g., different boards or tasks) reflects accurate, up-to-date data from the global context.

### Task 5: Maintain Predictability and Structure

Organize your actions and reducer logic so that future state changes are easy to understand and extend.

Document all available actions and how they affect the global state.

## Evaluation Criteria

| Area | Description | Weight |
|---|---|---|
| Context API Usage | Global state shared across all components effectively | 25% |
| Reducer Logic | State transitions defined and managed through clear actions | 25% |
| State Refactoring | Local states replaced with centralized global state | 20% |
| Synchronization | State remains consistent across routes and components | 15% |
| Code Quality | Clean, maintainable, and well-documented structure | 15% |

## Extension Challenge (Optional)

- Add an action to **move tasks** between columns and update global state dynamically.
- Implement **state persistence** using localStorage.
- Add a **theme toggle** (dark/light mode) managed by the same global state.
