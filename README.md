# React Router v6 Routing Issue with Nested and Wildcard Routes

This repository demonstrates a subtle bug in React Router v6 involving the interaction between nested routes and wildcard routes (`*`).  Specifically, the wildcard route interferes with the expected rendering of other routes.

## Problem
The issue arises when a wildcard route is defined alongside other more specific routes.  Navigation to a path that might match both the wildcard and a more specific route can result in incorrect rendering or unexpected routing behavior.  The provided example shows how the route `/contact/*` causes problems when other routes are defined in the same `Routes` component.

## Solution
The provided solution demonstrates a way to reorganize the routes to ensure that the wildcard route does not interfere with more specific paths.  This often involves prioritizing the order of routes or using more precise path matching strategies to avoid conflicts.