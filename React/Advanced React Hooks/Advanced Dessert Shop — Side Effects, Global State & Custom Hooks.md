# Advanced React Hooks: Advanced Dessert Shop
## Learning Objectives

By the end of this lab, you should be able to:

- **useEffect & Side Effects:** Handle data fetching, localStorage syncing, and reactive updates to state changes.
- **Context API:** Create and manage global state accessible across multiple components.
- **useReducer:** Simplify complex state logic (like cart management) using reducers.
- **useMemo & useCallback:** Optimize performance by preventing unnecessary renders and recalculations.
- **Custom Hooks:** Encapsulate and reuse logic for cleaner and more maintainable code.

## Introduction

You will add side effects, move the cart state to a **global context**, manage cart updates using a **reducer**, and use **custom hooks** to organize reusable logic.

By the end of this lab, your app will have improved performance, state persistence, and maintainable architecture — just like a real production-grade e-commerce frontend.

## Tasks

### Task 1: Manage Global Cart State with Context

- Create a **CartContext** that holds cart state and actions (addItem, removeItem, clearCart).
- Wrap your app in the CartProvider to share cart data across all components.
- Replace prop drilling with useContext to access the cart in Cart and DessertCard.

**Expected Result:** All components can access and update cart data globally, without passing props manually.

### Task 2: Simplify State Logic with useReducer

- Inside CartContext, replace useState with useReducer.
- Define a reducer to handle cart actions: ADD_ITEM, REMOVE_ITEM, CLEAR_CART.
- Ensure logic is centralized and easier to maintain as the app grows.

**Expected Result:** Adding, removing, or clearing desserts is handled by clear, predictable actions through the reducer.

### Task 3: Persist Cart with useEffect & Local Storage

- Use the useEffect hook to **save cart items to localStorage** whenever the cart changes.
- On initial render, **load saved cart data** back into state.
- Optionally, create a `useLocalStorage` custom hook to handle this logic cleanly.

**Expected Result:** When the user refreshes the page, the cart still retains previously added desserts.

### Task 4: Optimize Performance with useMemo & useCallback

- Use **useMemo** to memoize expensive calculations (like total cart value).
- Use **useCallback** to memoize event handler functions passed to child components.
- Test and confirm that components re-render only when necessary.

**Expected Result:** The app remains responsive and efficient, even with larger lists or frequent state updates.

### Task 5: Create and Use Custom Hooks

- Refactor reusable logic (like cart management or localStorage syncing) into **custom hooks**. For example:
  - `useCart()` — A helper hook to access and manipulate global cart state.
  - `useLocalStorage()` — Handles reading/writing data to localStorage.
- Import and use these hooks across your components for cleaner, reusable code.

**Expected Result:** Your logic becomes modular, testable, and easily shareable across multiple components.

## Evaluation Criteria (Peer Review)

| Criteria | Score | Description |
|---|---|---|
| useEffect & Side Effects | 20 | Effectively handles syncing data with localStorage and responding to state changes. |
| Context & Reducer | 20 | Global state is properly managed and reducer logic is clear and organized. |
| Performance Optimization | 20 | Uses useMemo and useCallback to minimize unnecessary re-renders and computations. |
| Custom Hooks | 20 | Encapsulates reusable logic effectively, improving readability and maintainability. |
| Code Quality & UI Integration | 20 | Clean, modular structure with clear component hierarchy and consistent behavior across the app. |

## Extension Challenge (Optional)

- Create a **notification banner** that appears briefly when a dessert is added to the cart.
- Add **filter and sorting functionality** (e.g., sort desserts by price or category).
- Use **React.memo** for further performance optimization in list rendering.
- Introduce a **Checkout Summary Page** managed via global state.
