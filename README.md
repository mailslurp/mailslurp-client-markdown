# REST API Documentation
MailSlurp is an email API that lets you create and control email accounts over HTTP without an SMTP mail server. You can call the API using an API Key and an HTTP client or use one of the official [SDK libraries](/developers/).

See the docs for more information: [REST Endpoint Documentation](https://www.mailslurp.com/docs/api/docs/Apis/)

{{<tip>}}
All API endpoints are relative to base URL `https://api.mailslurp.com` and should include `x-api-key` header that is your MailSlurp [API Key](https://app.mailslurp.com/).
{{</tip}}

## Quick Links

- [All API Endpoints](https://www.mailslurp.com/docs/api/docs/Apis)
- [Response and request Models](https://www.mailslurp.com/docs/api/docs/Models)
  
### Common controllers
- [EmailController](https://www.mailslurp.com/docs/api/docs/Apis/EmailControllerApi/) read or send email.
- [InboxController](https://www.mailslurp.com/docs/api/docs/Apis/InboxControllerApi/) create and manage email addresses.
- [WaitForController](https://www.mailslurp.com/docs/api/docs/Apis/WaitForControllerApi/) wait for emails to arrive.
- [WebhookController](https://www.mailslurp.com/docs/api/docs/Apis/WebhookForControllerApi/) create webhook and forwarding.
- [All controllers](https://www.mailslurp.com/docs/api/docs/Apis/)

### Other resources
- [Swagger UI](https://api.mailslurp.com/swagger-ui.html)
- [Open API Spec](https://api.mailslurp.com/v2/api-docs)
- [SDK Libraries](https://www.mailslurp.com/developers)

## Authentication
You must obtain an API Key for MailSlurp to call the API. [Create a free account](https://app.mailslurp.com/sign-up/) to do so. Include your API Key in requests with the `x-api-key` header or use an [SDK client](https://www.mailslurp.com/docs/) and configure it to use your API Key.

```bash
$ curl -H 'x-api-key:your_mailslurp_api_key' -X POST https://api.mailslurp.com/inboxes/
```

## Example usage

### Create email account
You can create and email address by making a `POST` request to the `/inboxes/` endpoint:

```bash
$ curl -H "x-api-key:$API_KEY" -X POST https://api.mailslurp.com/inboxes/
> {"id":"baefb45e-40ab-49fa-a0cb-2d41adc522b5","userId":"6f68f0cc-4760-4e82-87ad-449c9037773b","created":"2021-05-04T07:26:06.595Z","createdAt":"2021-05-04T07:26:06.595Z","name":null,"description":null,"emailAddress":"baefb45e-40ab-49fa-a0cb-2d41adc522b5@mailslurp.com","expiresAt":null,"favourite":false,"tags":null,"teamAccess":false,"readOnly":false}
```
See [endpoint documentation](https://www.mailslurp.com/docs/api/docs/Apis/) for more examples.

