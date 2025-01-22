# React Router Catch-all Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`*`) conflicts with other defined routes.  The problem arises when the catch-all route unintentionally intercepts navigation to paths that should be handled by more specific routes.

The `App.js` file contains the buggy code, while `AppSolution.js` provides a solution to resolve the conflict.

## Issue:

The catch-all route (`<Route path="*" element={<NotFound />} />`) is too broad and might intercept navigation intended for other routes, leading to the `NotFound` component being rendered even when a matching route exists. This commonly happens when a route has parameters or nested routes that create unexpected matches with the catch-all.

## Solution:

The solution is to reorder routes and make sure that the more specific routes are defined before the catch-all route to handle any potential conflicts. 
