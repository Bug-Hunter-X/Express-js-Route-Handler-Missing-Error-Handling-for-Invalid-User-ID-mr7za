# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  The provided code attempts to fetch a user based on a provided ID.  However, it fails to handle cases where the ID is not a valid integer, leading to potential crashes or unexpected behavior.  The solution demonstrates robust error handling to prevent this.

## Bug

The `bug.js` file contains the erroneous code.  It uses `parseInt` to convert the user ID but does not account for potential `NaN` results (Not a Number).  This leads to issues when an invalid ID is passed in, causing a runtime error or unexpected output.

## Solution

The `bugSolution.js` file demonstrates the corrected code. It now includes comprehensive error handling to check if the parsed ID is a valid integer and handles the case where the user is not found gracefully.