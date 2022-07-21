# Getting Started
New to Casual API? This is the right place. This page will describe how you can quickly
setup everything.

## Registration
Casual API requires authentication token for usage. This authentication token can be
retrieved for free by creating a new API account.

For creating an account, head over to [Registration Page](https://casual-api.herokuapp.com)
and create an account. The registration process is of course, quite straight forward.

Once registered, login to your account and you will be redirected to your dashboard.
From here, you can go to `Settings > Authentication` and copy your authentication token
from here.

!!! warning "Token Safety"

    Your authentication token can be used for malcious purposes. You should
    keep it safe and treat it like a password. In case it gets compromised,
    you can regenerate it from the same page.

## Base URL
```
https://casual-api.herokuapp.com/api
```

## Next Steps
You are now ready to make requests to the API. The next page,
[Authorization](../authorization) will guide you through the process of authenticating
your requests using the created authentication token.
