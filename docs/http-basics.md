# HTTP Basics Quickstart

## 1. Concept

HTTP (Hypertext Transfer Protocol) is the foundation of communication for web APIs. Clients send **requests** (GET, POST, etc.) to servers, which return **responses** containing status codes, headers, and body data.

---

## 2. Task: Practice with Postman

### ▶️ GET Request

1. **Setup**

   * Method: `GET`
   * URL: `https://postman-echo.com/get?user=Yash&purpose=learning`

2. **Send & Inspect**

   * Click **Send** in Postman
   * **Status**: `200 OK`

**Full Response Example**:

```json
{
  "args": {
    "user": "Yash",
    "purpose": "learning"
  },
  "headers": {
    "host": "postman-echo.com",
    "x-request-start": "t1752577778.554",
    "connection": "close",
    "x-forwarded-proto": "https",
    "x-forwarded-port": "443",
    "x-amzn-trace-id": "Root=1-687636f2-0c9dcfb6373518c23806dbb0",
    "user-agent": "PostmanRuntime/7.44.1",
    "accept": "*/*",
    "cache-control": "no-cache",
    "postman-token": "56a6908e-7395-44c6-979b-be1f0d1b003c",
    "accept-encoding": "gzip, deflate, br"
  },
  "url": "https://postman-echo.com/get?user=Yash&purpose=learning"
}
```

---

### ▶️ POST Request

1. **Setup**

   * Method: `POST`
   * URL: `https://postman-echo.com/post`
   * Body → **raw** → **JSON**:

   ```json
   {
     "name": "Yash Singh",
     "learning": "HTTP Basics",
     "goal": "Tech Writer"
   }
   ```

2. **Send & Inspect**

   * Click **Send**
   * **Status**: `200 OK`

**Full Response Example**:

```json
{
  "args": {},
  "data": {
    "name": "Yash Singh",
    "learning": "HTTP Basics",
    "goal": "Tech Writer"
  },
  "files": {},
  "form": {},
  "headers": {
    "host": "postman-echo.com",
    "x-request-start": "t1752577917.978",
    "connection": "close",
    "content-length": "86",
    "x-forwarded-proto": "https",
    "x-forwarded-port": "443",
    "x-amzn-trace-id": "Root=1-6876377d-63ecdcf9599b1ed7272bb3e6",
    "content-type": "application/json",
    "user-agent": "PostmanRuntime/7.44.1",
    "accept": "*/*",
    "cache-control": "no-cache",
    "postman-token": "4805bcfd-eed0-46a2-a322-4a98e7634908",
    "accept-encoding": "gzip, deflate, br",
    "cookie": "sails.sid=..."
  },
  "json": {
    "name": "Yash Singh",
    "learning": "HTTP Basics",
    "goal": "Tech Writer"
  },
  "url": "https://postman-echo.com/post"
}
```

---

## 3. Reference

* [MDN HTTP Overview](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
* [Postman Echo Documentation](https://docs.postman-echo.com/)