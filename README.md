# Uncaught ReferenceError: nonExistentVariable is not defined in Next.js 15

This repository demonstrates a common yet easily overlooked error in Next.js 15 applications: unhandled runtime errors in page components.  Accessing a variable that hasn't been defined results in an error that isn't gracefully handled by Next.js's default error boundaries, leading to a broken user experience.

## The Problem

The `about.js` file attempts to access a variable (`nonExistentVariable`) that doesn't exist in its scope, throwing a `ReferenceError`.  This error, if unhandled, will prevent the component from rendering correctly, resulting in a blank page or a 500 server error, depending on the environment.

## The Solution

The solution involves proper error handling within the component.  This can be achieved using a `try...catch` block or other suitable error handling mechanisms to gracefully manage the error and present a user-friendly message, or fallback to a default state.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm run dev` to start the development server.
5. Visit the `/about` page.  You should see the error.
