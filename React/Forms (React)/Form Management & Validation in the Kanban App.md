# React Forms: Form Management & Validation in the Kanban App
## Learning Objectives

By the end of this lab, you should be able to:

- Implement controlled form components to handle user input.
- Manage form data and validation using React Hook Form.
- Integrate form submissions with the global Kanban state.
- Display validation feedback and confirmation messages to enhance user experience.
- Maintain clean, modular form components that can scale with the application.

## Introduction

The focus of this lab is to make your app **interactive, accessible, and data-driven** — ensuring user input is validated and integrated seamlessly into your existing state management system.

By the end of the session, your Kanban app should allow users to **add and edit tasks** through structured forms that validate input and update the board dynamically.

## Tasks

### Task 1: Introduce Form Components

Create a new form component for handling **task creation** and **task editing**.

Ensure the form collects all necessary information such as title, description, status, and any additional task details your app supports.

The form should be consistent with the existing app design and accessible within the Kanban interface.

### Task 2: Use Controlled Form Inputs

Ensure that all form inputs are fully controlled and reflect the internal form state.

The form values should update in real-time as the user interacts with each field.

Maintain a consistent state structure that integrates smoothly with the app's global store.

### Task 3: Implement Form Validation

Introduce validation to ensure users provide valid and complete task information before submission.

The validation should include required fields and field-specific rules such as character limits or length constraints.

Provide clear feedback for validation errors directly within the form.

### Task 4: Connect Form to Global State

Integrate form submission with the existing global store (Redux or Zustand).

When a user submits a form, the global state should update accordingly — either creating a new task or editing an existing one.

Ensure updates are reflected instantly in the UI without requiring a page refresh.

### Task 5: Provide User Feedback

After successful submission, provide clear feedback to the user.

The form should reset or close automatically when an action is completed.

Display confirmation messages or visual indicators that communicate success or failure.

### Task 6: Ensure Accessibility & Usability

Ensure that the form is accessible through both keyboard and mouse interactions.

Make sure validation and success messages are perceivable by all users.

Test usability across multiple task actions to confirm a smooth workflow.

## Evaluation Criteria

| Criteria | Description | Weight |
|---|---|---|
| Controlled Components | Inputs are fully controlled and sync correctly with form state | 20% |
| Validation | Clear, effective validation with accessible error feedback | 25% |
| Integration | Form actions correctly update the global state | 25% |
| UX Feedback | Successful submissions provide clear and user-friendly feedback | 15% |
| Code Quality | Modular, clean, and maintainable component structure | 15% |

## Extension Challenge (Optional)

- Add form editing for existing tasks with preloaded data.
- Implement subtask management within the form.
- Provide live character counts for input fields.
- Add form-level validation summaries for multiple errors.
- Animate form submission success using subtle motion or transitions.
