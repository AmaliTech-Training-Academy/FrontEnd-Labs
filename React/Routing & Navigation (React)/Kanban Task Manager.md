# React Routing & Navigation: Kanban Task Manager
## Learning Objectives

By the end of this lab, you should be able to:

- **React Router Fundamentals:** Configure and manage client-side routing in a React app.
- **Dynamic Routing & Params:** Render dynamic pages and handle URL parameters.
- **Protected Routes:** Restrict access to specific pages based on authentication or state.
- **Nested Routes:** Organize complex page layouts with shared components and navigation.
- **Navigation State Management:** Sync route navigation with app state for consistent UX.

## Introduction

You'll integrate **React Router** to handle **multiple pages**, **dynamic boards**, and **protected routes** (like an Admin or Dashboard view).

By the end of this lab, you'll have a **multi-page React application** with persistent state, structured routing, and a scalable navigation system suitable for large real-world apps.

## Tasks

### Task 1: Set Up Routing Structure

- Wrap your app in `<BrowserRouter>` inside main.tsx.
- Define routes in App.tsx for:
  - `/` → Dashboard
  - `/board/:boardId` → BoardView
  - `/login` → Login page
  - `/admin` → Admin (Protected)
- Add a Header and Sidebar visible on all main routes.

**Expected Result:** The app supports client-side navigation between pages without full reloads.

### Task 2: Create Dynamic Routing for Boards

- In Dashboard.tsx, map over boards.json to display all boards.
- Each board should link to `/board/:boardId`.
- In BoardView.tsx, use `useParams()` to get the boardId and load the corresponding board data.

**Expected Result:** Selecting a board from the sidebar dynamically loads its tasks and columns.

### Task 3: Add Protected Routes

- Create an AuthContext with mock authentication (isLoggedIn, login, logout).
- Implement a ProtectedRoute component that checks isLoggedIn before rendering children.
- If unauthorized, redirect to `/login`.
- Protect routes like `/admin` or `/board/:boardId` as needed.

**Expected Result:** Users must be "logged in" to view specific routes like the Admin panel.

### Task 4: Handle Route Navigation and State Persistence

- Use `useNavigate()` to redirect users after login or logout.
- Persist login state with localStorage or Context.
- Highlight the active board in the sidebar based on the current route.

**Expected Result:** Navigation feels seamless and reflects real user sessions.

### Task 5: Create a NotFound Route

- Add a `*` route that renders a custom NotFound page.
- Include a "Go Back" or "Return to Dashboard" button.

**Expected Result:** Invalid URLs show a friendly 404 message with navigation options.

## Evaluation Criteria (Peer Review)

| Criteria | Score | Description |
|---|---|---|
| React Router Fundamentals | 20 | Routes configured correctly using `<BrowserRouter>`, `<Routes>`, and `<Route>`. |
| Dynamic Routing & Params | 20 | Correctly renders pages using URL parameters (useParams). |
| Protected Routes | 20 | Guards sensitive routes effectively and redirects unauthorized users. |
| Navigation & State Management | 20 | App state (auth, navigation) persists and syncs smoothly across routes. |
| Code Quality & Structure | 20 | Organized, modular code with readable and maintainable structure. |

## Extension Challenge (Optional)

- Add **nested routes** for managing columns or tasks within each board (e.g., `/board/:boardId/task/:taskId`).
- Animate route transitions using **Framer Motion**.
- Implement a **dark/light mode toggle** that persists across routes.
