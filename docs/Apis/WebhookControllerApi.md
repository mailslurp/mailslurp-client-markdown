# WebhookControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createWebhook**](WebhookControllerApi#createWebhook) | **POST** /inboxes/{inboxId}/webhooks | Attach a WebHook URL to an inbox
[**deleteWebhook**](WebhookControllerApi#deleteWebhook) | **DELETE** /inboxes/{inboxId}/webhooks/{webhookId} | Delete and disable a Webhook for an Inbox
[**getAllWebhookResults**](WebhookControllerApi#getAllWebhookResults) | **GET** /webhooks/results | Get results for all webhooks
[**getAllWebhooks**](WebhookControllerApi#getAllWebhooks) | **GET** /webhooks/paginated | List Webhooks Paginated
[**getInboxWebhooksPaginated**](WebhookControllerApi#getInboxWebhooksPaginated) | **GET** /inboxes/{inboxId}/webhooks/paginated | Get paginated webhooks for an Inbox
[**getTestWebhookPayload**](WebhookControllerApi#getTestWebhookPayload) | **GET** /webhooks/test | Get test webhook payload example. Response content depends on eventName passed. Uses &#x60;EMAIL_RECEIVED&#x60; as default.
[**getTestWebhookPayloadEmailOpened**](WebhookControllerApi#getTestWebhookPayloadEmailOpened) | **GET** /webhooks/test/email-opened-payload | Get webhook test payload for email opened event
[**getTestWebhookPayloadNewAttachment**](WebhookControllerApi#getTestWebhookPayloadNewAttachment) | **GET** /webhooks/test/new-attachment-payload | Get webhook test payload for new attachment event
[**getTestWebhookPayloadNewContact**](WebhookControllerApi#getTestWebhookPayloadNewContact) | **GET** /webhooks/test/new-contact-payload | Get webhook test payload for new contact event
[**getTestWebhookPayloadNewEmail**](WebhookControllerApi#getTestWebhookPayloadNewEmail) | **GET** /webhooks/test/new-email-payload | Get webhook test payload for new email event
[**getWebhook**](WebhookControllerApi#getWebhook) | **GET** /webhooks/{webhookId} | Get a webhook for an Inbox
[**getWebhookResult**](WebhookControllerApi#getWebhookResult) | **GET** /webhooks/results/{webhookResultId} | Get a webhook result for a webhook
[**getWebhookResults**](WebhookControllerApi#getWebhookResults) | **GET** /webhooks/{webhookId}/results | Get a webhook results for a webhook
[**getWebhooks**](WebhookControllerApi#getWebhooks) | **GET** /inboxes/{inboxId}/webhooks | Get all webhooks for an Inbox
[**sendTestData**](WebhookControllerApi#sendTestData) | **POST** /webhooks/{webhookId}/test | Send webhook test data


<a name="createWebhook"></a>
# **createWebhook**
> WebhookDto createWebhook(inboxId, webhookOptions)

Attach a WebHook URL to an inbox

    Get notified whenever an inbox receives an email via a WebHook URL. An emailID will be posted to this URL every time an email is received for this inbox. The URL must be publicly reachable by the MailSlurp server. You can provide basicAuth values if you wish to secure this endpoint.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| inboxId | [default to null]
 **webhookOptions** | [**CreateWebhookOptions**](../Models/CreateWebhookOptions)| webhookOptions |

### Return type

[**WebhookDto**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteWebhook"></a>
# **deleteWebhook**
> deleteWebhook(inboxId, webhookId)

Delete and disable a Webhook for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| inboxId | [default to null]
 **webhookId** | [**UUID**](../Models/)| webhookId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllWebhookResults"></a>
# **getAllWebhookResults**
> PageWebhookResult getAllWebhookResults(page, searchFilter, size, sort)

Get results for all webhooks

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageWebhookResult**](../Models/PageWebhookResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAllWebhooks"></a>
# **getAllWebhooks**
> PageWebhookProjection getAllWebhooks(page, searchFilter, size, sort)

List Webhooks Paginated

    List webhooks in paginated form. Allows for page index, page size, and sort direction.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageWebhookProjection**](../Models/PageWebhookProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxWebhooksPaginated"></a>
# **getInboxWebhooksPaginated**
> PageWebhookProjection getInboxWebhooksPaginated(inboxId, page, searchFilter, size, sort)

Get paginated webhooks for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| inboxId | [default to null]
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageWebhookProjection**](../Models/PageWebhookProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTestWebhookPayload"></a>
# **getTestWebhookPayload**
> AbstractWebhookPayload getTestWebhookPayload(eventName)

Get test webhook payload example. Response content depends on eventName passed. Uses &#x60;EMAIL_RECEIVED&#x60; as default.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **eventName** | **String**| eventName | [optional] [default to null] [enum: EMAIL_RECEIVED, NEW_EMAIL, NEW_CONTACT, NEW_ATTACHMENT, EMAIL_OPENED]

### Return type

[**AbstractWebhookPayload**](../Models/AbstractWebhookPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTestWebhookPayloadEmailOpened"></a>
# **getTestWebhookPayloadEmailOpened**
> WebhookEmailOpenedPayload getTestWebhookPayloadEmailOpened()

Get webhook test payload for email opened event

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookEmailOpenedPayload**](../Models/WebhookEmailOpenedPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTestWebhookPayloadNewAttachment"></a>
# **getTestWebhookPayloadNewAttachment**
> WebhookNewAttachmentPayload getTestWebhookPayloadNewAttachment()

Get webhook test payload for new attachment event

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookNewAttachmentPayload**](../Models/WebhookNewAttachmentPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTestWebhookPayloadNewContact"></a>
# **getTestWebhookPayloadNewContact**
> WebhookNewContactPayload getTestWebhookPayloadNewContact()

Get webhook test payload for new contact event

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookNewContactPayload**](../Models/WebhookNewContactPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTestWebhookPayloadNewEmail"></a>
# **getTestWebhookPayloadNewEmail**
> WebhookNewEmailPayload getTestWebhookPayloadNewEmail()

Get webhook test payload for new email event

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookNewEmailPayload**](../Models/WebhookNewEmailPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getWebhook"></a>
# **getWebhook**
> WebhookDto getWebhook(webhookId)

Get a webhook for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)| webhookId | [default to null]

### Return type

[**WebhookDto**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getWebhookResult"></a>
# **getWebhookResult**
> WebhookResultEntity getWebhookResult(webhookResultId)

Get a webhook result for a webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookResultId** | [**UUID**](../Models/)| Webhook Result ID | [default to null]

### Return type

[**WebhookResultEntity**](../Models/WebhookResultEntity)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getWebhookResults"></a>
# **getWebhookResults**
> PageWebhookResult getWebhookResults(webhookId, page, searchFilter, size, sort)

Get a webhook results for a webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)| ID of webhook to get results for | [default to null]
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageWebhookResult**](../Models/PageWebhookResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getWebhooks"></a>
# **getWebhooks**
> List getWebhooks(inboxId)

Get all webhooks for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| inboxId | [default to null]

### Return type

[**List**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="sendTestData"></a>
# **sendTestData**
> WebhookTestResult sendTestData(webhookId)

Send webhook test data

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)| webhookId | [default to null]

### Return type

[**WebhookTestResult**](../Models/WebhookTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

