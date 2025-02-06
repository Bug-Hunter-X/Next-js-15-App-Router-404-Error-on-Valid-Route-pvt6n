# Next.js 15 App Router 404 Error on Valid Route

This repository demonstrates a bug in Next.js 15's App Router where a 404 error is unexpectedly returned when navigating to a page that clearly exists within the application's file structure. The bug is related to how the new router handles route resolution in the app directory.

## Steps to Reproduce

1. Clone the repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Navigate to the `/` route. You should see the expected 'Hello' message.
5. Observe that navigating to other routes consistently produces a 404 error. 

## Expected Behavior

Navigating to valid routes within the app directory should render the corresponding page component without throwing a 404 error.

## Actual Behavior

A 404 error is returned for all routes other than the root (`/`) route, despite the presence of corresponding files and folders within the `app` directory.

## Solution

The issue stems from an improper configuration of the app directory or possibly a bug in the Next.js router itself.  The solution provided in `bugSolution.js` may not be applicable to all instances, but it addresses the specific issue encountered here.  This usually involves verifying that the routing structure follows Next.js conventions and ensuring no conflicting routes exist.