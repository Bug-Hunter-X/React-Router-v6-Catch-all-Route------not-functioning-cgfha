# React Router v6 Catch-all Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6.  Specifically, the catch-all route fails to render when an invalid URL is accessed, even though other routes work correctly.

## Problem Description

The application uses React Router v6 to define several routes, including a catch-all route intended to handle 404 scenarios. However, the catch-all route does not trigger, leading to a blank screen or unexpected behavior.

## Solution

The issue is resolved by ensuring the catch-all route (`/*`) is placed *after* all other specific routes within the `<Routes>` component.  This ensures that the catch-all route only activates when no other routes match the URL.

## How to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Navigate to a non-existent URL (e.g., `/invalid-route`).  Observe that the catch-all route does not render.

## Note

This example highlights a common pitfall in using React Router v6's route matching.  Careful ordering and placement of routes are crucial for correct functionality.