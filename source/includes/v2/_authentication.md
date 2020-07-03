# Authentication

The Popdock API uses user tokens for authentication. New authentication tokens can be geenrated in Popodock from any user's profile page.

The token will passed as a Bearer Token header with all api requests.

```json
{"error": "Invalid token"}
```

![User Token](images/User_Token.jpg)

<aside class="notice">
Tokens are user specific, they are the security equivalent of a user accessing the data through the Popdock web client.
</aside>
