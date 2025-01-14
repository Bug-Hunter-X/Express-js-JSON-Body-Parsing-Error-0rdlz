# Express.js JSON Body Parsing Error

This repository demonstrates a common error in Express.js applications where the request body is not parsed correctly when the `Content-Type` header is missing or incorrect.

## Bug
The bug lies in the `app.post` route handler.  It assumes that the request body will always be parsed as JSON, regardless of the `Content-Type` header.

## Solution
The solution is to always explicitly check and set the `Content-Type` header in the client request.  The server-side code should also include error handling to catch situations where the `Content-Type` header is incorrect or missing.