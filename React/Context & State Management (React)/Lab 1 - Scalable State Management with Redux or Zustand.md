## Learning Objectives

By the end of this lab, you should be able to:

- Set up a **state management library** (Zustand or Redux) for predictable, global state control.
- Store and manage Kanban data (boards, columns, tasks) in a **central store**.
- Update UI reactively based on global state changes without prop drilling.
- Implement **immutable state updates** and **persistent storage**.
- Understand how external libraries improve scalability compared to Context or local state.

## Introduction

This approach will prepare your app for handling more complex features like user authentication, multiple boards, and collaborative updates.

## Project Overview

You'll extend your **Kanban Board App** from Lab 4.1 by introducing a **central store** to manage boards and columns, tasks and their statuses, and UI preferences (like dark mode or selected board).

Your main goal is to **move all shared state** from components or context into a **dedicated store**, allowing any part of your app to access and update state easily.

## Tasks

### Task 1: Initialize the Store

Create a store (using Zustand or Redux) to manage your Kanban data.

The store should contain boards, columns, and tasks as the main data entities.

> **Hint:** Treat the store as the single source of truth — all updates must go through it.

### Task 2: Define Core State and Actions

Add actions to handle common Kanban interactions such as:
- Adding, updating, or deleting tasks
- Moving tasks between columns
- Creating or removing columns or boards

Keep your actions minimal and focused. They should describe *what* happens, not *how*.

### Task 3: Connect Components to the Store

Refactor your existing components (e.g., BoardView, TaskList, TaskCard) to:
- Read state directly from the store
- Dispatch updates via actions instead of using local state

Avoid prop drilling — all data should flow from the global store.

### Task 4: Persist State Between Sessions

Enable persistence using either:
- **localStorage** (manually syncing state), or
- a built-in middleware (e.g., `persist` in Zustand)

This ensures your Kanban data is not lost after page refreshes.

### Task 5: Optimize and Maintain State Integrity

Ensure your store:
- Handles immutable updates
- Prevents data duplication or stale references
- Supports reactive UI updates with minimal re-renders

## Evaluation Criteria

| Area | Description | Weight |
|---|---|---|
| Store Structure | Centralized and organized state definition | 25% |
| Actions & Updates | Clear, consistent state update logic | 25% |
| Component Integration | Components consume store data correctly | 20% |
| Persistence | State is saved and restored properly | 15% |
| Code Quality & Structure | Modular, scalable, and easy to read | 15% |

## Extension Challenge (Optional)

- Add **drag-and-drop functionality** for moving tasks (e.g., with @dnd-kit or react-beautiful-dnd).
- Introduce a **theme toggle** stored in global state.
