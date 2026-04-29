# React Fundamentals: Dessert Shop App
## Learning Objectives

By the end of this lab, you should be able to:

- **JSX & Rendering:** Build and render reusable UI components using JSX syntax.
- **Components & Props:** Pass and use props effectively to display dynamic dessert data in components.
- **State & Events:** Manage component state to track user actions (like adding to cart) and update the UI in real time.
- **UI Interactivity:** Provide a seamless and responsive shopping experience that reacts instantly to user input.
- Deploy and share their project via GitHub and Vercel/Netlify.

## Introduction

In this lab, you will build a **Dessert Shop App** — a mini e-commerce interface where users can browse desserts and add them to their cart.

You'll explore how **JSX**, **props**, and **state** come together to build modular, interactive user interfaces in React.

By the end of this lab, your app should allow users to add and remove desserts, dynamically update totals, and display an engaging, responsive layout that sets the foundation for upcoming labs on useEffect, useMemo, and custom hooks.

## Tasks

### Task 1: Build a Reusable DessertCard Component

- Create a card layout for each dessert that displays its image, name, and price.
- Use props to make the card reusable for multiple dessert items.
- Add a button for "Add to Cart" and handle interactions through props.
- Provide fallback messages when data (e.g., image or price) is missing.

### Task 2: Render the Dessert List

- Display multiple desserts by mapping through a dessert data array.
- Pass each dessert's data as props to the DessertCard component.
- Organize cards in a responsive grid layout to enhance the user experience.

### Task 3: Manage Cart State

- Use state to track selected desserts in the cart.
- Update the cart when the user adds or removes a dessert.
- Prevent duplicate items by disabling or visually marking items already in the cart.
- Display the number of desserts added to the cart.

### Task 4: Create the Cart Component

- Display added desserts, their prices, and the overall total.
- Include options to remove specific items or clear the entire cart.
- Provide a checkout-like interface with a total summary and visual feedback.

### Task 5: Integrate Components

- Combine all components (DessertList, DessertCard, Cart) within the main App component.
- Ensure state flows correctly between components and updates are reflected instantly.
- Confirm that user interactions (adding/removing desserts) dynamically update the total and cart count.

## Styling and Layout

- Apply CSS / SCSS (optional).
- Ensure responsiveness by testing on various screen sizes.
- Match the **Product List with Cart** layout as closely as possible.

## Evaluation Criteria (Peer Review)

| Criteria | Score | Description |
|---|---|---|
| JSX & Rendering | 25 | Components render correctly using clean and structured JSX. Conditional rendering is used effectively. |
| Components & Props | 25 | Props are used appropriately to pass and display data. Components are reusable and modular. |
| State & Events | 25 | State updates dynamically with user interactions. Event handling logic works as expected. |
| Code Quality & UI Integration | 25 | Code is organized, readable, and follows React best practices. UI updates and user feedback enhance the overall experience. |

## Extension Challenge (Optional)

- Add a quantity selector for each dessert in the cart.
- Show an estimated total with tax or delivery fees.
- Display an "In Cart" badge on items already added.
- Persist cart data using localStorage for session retention.
- Add subtle animations for adding/removing items to enhance interactivity.
