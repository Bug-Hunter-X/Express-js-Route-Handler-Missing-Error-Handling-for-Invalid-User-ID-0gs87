# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code attempts to parse a user ID from a route parameter as an integer without checking if the parameter is actually a number. This can lead to unexpected behavior or crashes if a non-numeric ID is provided.

## Bug

The `bug.js` file contains the erroneous code.  It attempts to find a user based on an ID obtained from the route parameters. However, it lacks error handling for scenarios where the provided ID is not a valid number.  This can result in a `NaN` comparison and potentially cause the application to crash or return unexpected results.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes input validation to ensure the `userId` parameter is a number before attempting to use it.  Appropriate error handling is implemented using a `try...catch` block to gracefully handle potential errors during type conversion and user lookup.