# OAuth 2.0 Quickstart for Fintech APIs

## 1. Concept
OAuth 2.0 is an industry-standard authorization framework that enables fintech applications to obtain secure, scoped access to user data on HTTP services without handling user passwords directly. It issues time-limited tokens that your application can use as credentials for subsequent API calls.
## 2. Task: Get an Access Token
To obtain an access token using the Client Credentials flow:

```http
POST https://oauth.example.com/token
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials&
client_id=YOUR_CLIENT_ID&
client_secret=YOUR_CLIENT_SECRET
{
  "access_token": "eyJhbGciOiJSUzI1NiIsInR5cCI...",
  "token_type": "Bearer",
  "expires_in": 3600
}
Steps:

Send a POST request to the token endpoint with your credentials.

Extract the access_token from the JSON response.

Include Authorization: Bearer <access_token> on future API calls.
## 3.Reference
| Parameter     | Type   | Description                          |
|---------------|--------|--------------------------------------|
| grant_type    | string | Must be `client_credentials` flow    |
| client_id     | string | Your application’s client ID         |
| client_secret | string | Your application’s client secret     |