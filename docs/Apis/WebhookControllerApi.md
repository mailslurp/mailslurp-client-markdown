# WebhookControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createWebhook**](WebhookControllerApi#createWebhook) | **POST** /inboxes/{inboxId}/webhooks | Attach a WebHook URL to an inbox
[**deleteWebhook**](WebhookControllerApi#deleteWebhook) | **DELETE** /inboxes/{inboxId}/webhooks/{webhookId} | Delete and disable a Webhook for an Inbox
[**getAllWebhooks**](WebhookControllerApi#getAllWebhooks) | **GET** /webhooks/paginated | List Webhooks Paginated
[**getWebhook**](WebhookControllerApi#getWebhook) | **GET** /webhooks/{webhookId} | Get a webhook for an Inbox
[**getWebhooks**](WebhookControllerApi#getWebhooks) | **GET** /inboxes/{inboxId}/webhooks | Get all Webhooks for an Inbox
[**sendTestData**](WebhookControllerApi#sendTestData) | **POST** /webhooks/{webhookId}/test | Send webhook test data


<a name="createWebhook"></a>
# **createWebhook**
> WebhookDto createWebhook(inboxId, webhookOptions)

Attach a WebHook URL to an inbox

    Get notified whenever an inbox receives an email via a WebHook URL. An emailID will be posted to this URL every time an email is received for this inbox. The URL must be publicly reachable by the MailSlurp server. You can provide basicAuth values if you wish to secure this endpoint.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]
 **webhookOptions** | [**CreateWebhookOptions**](..//Models/CreateWebhookOptions)| webhookOptions |

### Return type

[**WebhookDto**](..//Models/WebhookDto)

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
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]
 **webhookId** | [**UUID**](..//Models/)| webhookId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllWebhooks"></a>
# **getAllWebhooks**
> PageWebhookProjection getAllWebhooks(page, size, sort)

List Webhooks Paginated

    List webhooks in paginated form. Allows for page index, page size, and sort direction.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in inbox list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageWebhookProjection**](..//Models/PageWebhookProjection)

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
 **webhookId** | [**UUID**](..//Models/)| webhookId | [default to null]

### Return type

[**WebhookDto**](..//Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getWebhooks"></a>
# **getWebhooks**
> List getWebhooks(inboxId)

Get all Webhooks for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]

### Return type

[**List**](..//Models/WebhookDto)

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
 **webhookId** | [**UUID**](..//Models/)| webhookId | [default to null]

### Return type

[**WebhookTestResult**](..//Models/WebhookTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

