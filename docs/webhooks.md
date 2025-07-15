# Webhooks Quickstart

## 1. Concept

Webhooks are HTTP callbacks: when a specific event occurs, Service A pushes an HTTP POST to your endpoint (Service B) in real time—no polling needed.

## 2. Task: Receive a Webhook

1. **Listener Setup**  
   - Obtained a free listener URL from [webhook.site](https://webhook.site):  
     `https://webhook.site/2e1a8c77-0ebe-4606-a798-f7525aeb7742

2. **Send the Webhook**  
   ```http
   POST https://webhook.site/1234-abcd-5678-efgh
   Content-Type: application/json

   {
     "event": "invoice.paid",
     "data": {
       "invoice_id": "inv_1001",
       "amount": 4999,
       "currency": "INR"
     }
   }
Click Send in Postman.

3. **Inspect the Payload**

a.On webhook.site, view the Recent Requests list.

b.Confirm headers and JSON body match your POST.
## 3. Reference
**webhook.site**

a.webhook.site

b.What Are Webhooks? – Write the Docs

