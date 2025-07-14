# OAuth 2.0 Tutorial
## 1. Concept
OAuth 2.0 is an authorization framework that lets users grant limited access to their resources on one site (e.g., Google) to another site (e.g., a calendar app) — without sharing their password.

It is used when an app wants to access user data (like your Gmail or Facebook profile) on your behalf.
## 2. Task: Get an Access Token Using Postman
### Step-by-Step:
1. Open Postman → click `+` to create a new request.
2. In the request:
   - Method: `POST`
   - URL: `https://oauth.pstmn.io/v1/token`
3. Click on **Authorization tab**:
   - Type: `OAuth 2.0`
   - Click `Get New Access Token`
   - Fill in:
     - Grant Type: `Client Credentials`
     - Access Token URL: `https://oauth.pstmn.io/v1/token`
     - Client ID: `postman`
     - Client Secret: `password`
     - Leave rest blank → Click `Get Token`
4. Select the token in the bottom and click **Use Token**.
5. Click `Send` to make the request.
For this task, I simulated an OAuth 2.0 token using Postman's built-in mock service.

- Endpoint used: `https://postman-echo.com/get`
- Token: `12345-fake-token-value`
- Authorization: Bearer Token
- Response: 200 OK with headers confirming token was included

![Postman Screenshot](path/to/screenshot.png)

You should see a JSON response with `access_token`

![Example response screenshot](https://user-images.githubusercontent.com/12205711/150681164-c40ee2fc-9ac4-4227-9702-f9a2e9f2e457.png)
## 3. Reference
- [OAuth 2.0 - oauth.com](https://www.oauth.com/oauth2-servers/access-tokens/)
- [Postman OAuth Docs](https://learning.postman.com/docs/sending-requests/authorization/#oauth-20)
