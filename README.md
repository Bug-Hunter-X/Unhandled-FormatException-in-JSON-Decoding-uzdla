# Unhandled FormatException in JSON Decoding

This repository demonstrates a common error in Dart when decoding JSON responses from APIs. The provided code snippet attempts to decode a JSON response without sufficient error handling, specifically failing to handle instances where the response body is not valid JSON.

## The Problem

The `jsonDecode` function from the `dart:convert` library throws a `FormatException` if the input string is not valid JSON.  If this exception is not caught and handled, your application will crash.

## The Solution

The solution involves adding robust error handling using `try-catch` blocks to gracefully manage the `FormatException` and prevent application crashes.  The updated code includes checks for `response.statusCode` to ensure the API request was successful before attempting JSON decoding.
