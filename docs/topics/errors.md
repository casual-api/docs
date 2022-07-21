# Errors Format
Whenever client sends an invalid request, API will respond with a consistently formated
error. This error format is guaranteed to be consistent on all API endpoints.

|     Field     |  Type  |        Description        |
|:-------------:|:------:|:-------------------------:|
|    `detail`   | string |    The detail of error    |
|    `hint`?    | string | A hint for this error fix |

`hint` is only included for errors that are known to be *common yet not so obvious*.

**Example:**
```json
{
    "details": "Missing JSON field: item",
    "hint": "Add an item field in JSON body with value of 1"
}
```

## Status Codes
The API uses [standard HTTP status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
to indicate the type of response.
