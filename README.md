# React Router Wildcard Route Issue

This repository demonstrates a common issue encountered when using wildcard routes (`/*`) in React Router.  The problem arises when a wildcard route is placed after other specific routes. Because the wildcard route matches any path, it will always be selected, preventing access to the other routes.

## Problem Description

The issue is that, due to the order of routes in the `Routes` component, the wildcard catch-all route (`/*`) always takes precedence, regardless of the path.  This causes every route to resolve to the catch-all route.

## Solution

The solution involves ordering the routes strategically. The wildcard route should always be the last route defined in the `Routes` component. This ensures that specific routes are matched before the wildcard route. 
