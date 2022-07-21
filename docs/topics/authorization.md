# Authorization
Casual API requires a token for authorizing the HTTP requests performed against the API. This
token is retrieved by creating an accout, described in previous page.

## Headers
The authorization token is sent by using the `Authorization` header. All clients should add
this header to requests when performing requests. The format for value of this header
is:
```
Authorization: Basic <AUTH-TOKEN-HERE>
```

## Errors
If the provided token in `Authorization` is invalid or the header is missing from requests or
is malformed (sent in invalid format), API will respond with `401` status.

```json
{
    "details": "Unauthorized"
}
```
