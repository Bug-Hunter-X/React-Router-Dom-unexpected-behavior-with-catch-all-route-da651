# React Router Dom unexpected behavior with catch all route

This repository demonstrates an unexpected behavior in React Router Dom v6 with the catch-all route `/*`. The catch-all route is unexpectedly matching all routes, even though other, more specific routes are defined before it.

## Bug Description
The issue occurs when combining a catch-all route (`/*`) with other more specific routes. The catch-all route intercepts all requests, even if a more specific route exists. This is counterintuitive and can lead to unexpected application behavior.

## Solution
The solution is to move the catch-all route to the last position in the routes array. This ensures that more specific routes are matched first, before the catch-all route is used for any unmatched paths. This ensures that more specific paths are evaluated first and only the unmatched paths go to the catch-all route.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/`, `/about`, etc. Notice that the catch-all route is always activated.

## How to fix
1. Clone this repository.
2. Run `npm install`.
3. Check the file `AppSolution.js` for the correct implementation.