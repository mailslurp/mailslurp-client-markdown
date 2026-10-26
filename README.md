# REST API Documentation

MailSlurp is an email API that lets you create and control email accounts over HTTP without an SMTP mail server. You can call the API using an API Key and an HTTP client or use one of the official [SDK libraries](/developers/).

## Resources

- [Swagger UI](https://api.mailslurp.com/swagger-ui.html)
- [Open API Spec](https://api.mailslurp.com/v2/api-docs)
- [Postman Collection](https://www.postman.com/mailslurp-api/workspace/mailslurp-email-api/overview)

## Authentication

You must obtain an API Key for MailSlurp to call the API. [Create a free account](https://app.mailslurp.com/sign-up/) to do so. Include your API Key in requests with the `x-api-key` header or use an [SDK client](https://docs.mailslurp.com/) and configure it to use your API Key.

```bash
curl -H 'x-api-key:your_mailslurp_api_key' -X POST https://api.mailslurp.com/inboxes/
```

!!swagger api.json!!
