# React HTTP & APIs: Data Fetching, Effecting & Async States
## Learning Objectives

By the end of this lab, you should be able to:

- Fetch data from an external API using fetch or axios.
- Manage asynchronous operations using useEffect.
- Handle loading and error states to improve user experience.
- Integrate fetched data into the Kanban app's global state.
- Maintain a clean, resilient data flow that reacts to API state changes.

## Introduction

In this lab, you will evolve your Kanban Task Management App into a data-driven application.

Instead of relying solely on static or local data, you'll fetch real task and board data from an API and handle asynchronous loading gracefully.

By the end of this lab, your Kanban app should dynamically display board data from a remote source and provide responsive feedback during loading or error states.

## Tasks

### Task 1: Set Up API Communication

Connect your Kanban application to a mock or real API endpoint that provides data for boards, columns, and tasks.

Ensure your global state or context can handle fetched data updates and reactivity.

Your app should load this data automatically when the user first visits the dashboard.

### Task 2: Implement Data Fetching with useEffect

Use React's useEffect hook to trigger data fetching when the component mounts.

Ensure your fetch or axios call runs only when necessary (e.g., when dependencies change).

The UI should reflect data loading in real time.

### Task 3: Handle Loading & Error States

Provide visual feedback while data is being fetched — such as a loading spinner, skeletons, or placeholder UI.

If an error occurs during fetching, show a clear and user-friendly error message.

Allow users to retry fetching data if the operation fails.

### Task 4: Integrate with Global State

Once data is successfully fetched, update your global store (Redux or Zustand) so that the data becomes accessible throughout the app.

Ensure that components relying on board or task data render correctly after the store updates.

### Task 5: Replace Static Data

Remove or replace any hardcoded task or board data that was used in earlier labs.

The app should now rely entirely on API-provided data.

Confirm that navigation, task updates, and board switching continue to function as expected.

### Task 6: Ensure a Smooth User Experience

Your app should always provide visual cues about what's happening — loading, success, or failure.

Make sure transitions between these states feel smooth and predictable.

Test with slow network speeds or simulated delays to ensure your loading UX is solid.

## Evaluation Criteria

| Criteria | Description | Weight |
|---|---|---|
| API Integration | App successfully fetches data and connects to the API | 25% |
| useEffect Usage | Correct use of effects for fetching and dependency management | 20% |
| Loading & Error States | Smooth and informative user feedback for async states | 25% |
| Global State Integration | Fetched data updates and syncs correctly with the store | 20% |
| Code Quality | Clean, modular, and readable implementation | 10% |
