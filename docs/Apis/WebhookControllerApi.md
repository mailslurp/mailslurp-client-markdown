# WebhookControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAccountWebhook**](WebhookControllerApi#createAccountWebhook) | **POST** /webhooks | Attach a WebHook URL to an inbox
[**createWebhook**](WebhookControllerApi#createWebhook) | **POST** /inboxes/{inboxId}/webhooks | Attach a WebHook URL to an inbox
[**deleteAllWebhooks**](WebhookControllerApi#deleteAllWebhooks) | **DELETE** /webhooks | Delete all webhooks
[**deleteWebhook**](WebhookControllerApi#deleteWebhook) | **DELETE** /inboxes/{inboxId}/webhooks/{webhookId} | Delete and disable a Webhook for an Inbox
[**deleteWebhookById**](WebhookControllerApi#deleteWebhookById) | **DELETE** /webhooks/{webhookId} | Delete a webhook
[**getAllWebhookResults**](WebhookControllerApi#getAllWebhookResults) | **GET** /webhooks/results | Get results for all webhooks
[**getAllWebhooks**](WebhookControllerApi#getAllWebhooks) | **GET** /webhooks/paginated | List Webhooks Paginated
[**getInboxWebhooksPaginated**](WebhookControllerApi#getInboxWebhooksPaginated) | **GET** /inboxes/{inboxId}/webhooks/paginated | Get paginated webhooks for an Inbox
[**getJsonSchemaForWebhookPayload**](WebhookControllerApi#getJsonSchemaForWebhookPayload) | **POST** /webhooks/{webhookId}/schema | 
[**getTestWebhookPayload**](WebhookControllerApi#getTestWebhookPayload) | **GET** /webhooks/test | 
[**getTestWebhookPayloadBounce**](WebhookControllerApi#getTestWebhookPayloadBounce) | **GET** /webhooks/test/email-bounce-payload | 
[**getTestWebhookPayloadBounceRecipient**](WebhookControllerApi#getTestWebhookPayloadBounceRecipient) | **GET** /webhooks/test/email-bounce-recipient-payload | 
[**getTestWebhookPayloadEmailOpened**](WebhookControllerApi#getTestWebhookPayloadEmailOpened) | **GET** /webhooks/test/email-opened-payload | 
[**getTestWebhookPayloadEmailRead**](WebhookControllerApi#getTestWebhookPayloadEmailRead) | **GET** /webhooks/test/email-read-payload | 
[**getTestWebhookPayloadForWebhook**](WebhookControllerApi#getTestWebhookPayloadForWebhook) | **POST** /webhooks/{webhookId}/example | 
[**getTestWebhookPayloadNewAttachment**](WebhookControllerApi#getTestWebhookPayloadNewAttachment) | **GET** /webhooks/test/new-attachment-payload | Get webhook test payload for new attachment event
[**getTestWebhookPayloadNewContact**](WebhookControllerApi#getTestWebhookPayloadNewContact) | **GET** /webhooks/test/new-contact-payload | Get webhook test payload for new contact event
[**getTestWebhookPayloadNewEmail**](WebhookControllerApi#getTestWebhookPayloadNewEmail) | **GET** /webhooks/test/new-email-payload | Get webhook test payload for new email event
[**getWebhook**](WebhookControllerApi#getWebhook) | **GET** /webhooks/{webhookId} | Get a webhook
[**getWebhookResult**](WebhookControllerApi#getWebhookResult) | **GET** /webhooks/results/{webhookResultId} | Get a webhook result for a webhook
[**getWebhookResults**](WebhookControllerApi#getWebhookResults) | **GET** /webhooks/{webhookId}/results | Get a webhook results for a webhook
[**getWebhookResultsUnseenErrorCount**](WebhookControllerApi#getWebhookResultsUnseenErrorCount) | **GET** /webhooks/results/unseen-count | Get count of unseen webhook results with error status
[**getWebhooks**](WebhookControllerApi#getWebhooks) | **GET** /inboxes/{inboxId}/webhooks | Get all webhooks for an Inbox
[**redriveWebhookResult**](WebhookControllerApi#redriveWebhookResult) | **POST** /webhooks/results/{webhookResultId}/redrive | Get a webhook result and try to resend the original webhook payload
[**sendTestData**](WebhookControllerApi#sendTestData) | **POST** /webhooks/{webhookId}/test | Send webhook test data


<a name="createAccountWebhook"></a>
# **createAccountWebhook**
> WebhookDto createAccountWebhook(CreateWebhookOptions)

Attach a WebHook URL to an inbox

    Get notified of account level events such as bounce and bounce recipient.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateWebhookOptions** | [**CreateWebhookOptions**](../Models/CreateWebhookOptions)|  |

### Return type

[**WebhookDto**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="createWebhook"></a>
# **createWebhook**
> WebhookDto createWebhook(inboxId, CreateWebhookOptions)

Attach a WebHook URL to an inbox

    Get notified whenever an inbox receives an email via a WebHook URL. An emailID will be posted to this URL every time an email is received for this inbox. The URL must be publicly reachable by the MailSlurp server. You can provide basicAuth values if you wish to secure this endpoint.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]
 **CreateWebhookOptions** | [**CreateWebhookOptions**](../Models/CreateWebhookOptions)|  |

### Return type

[**WebhookDto**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="deleteAllWebhooks"></a>
# **deleteAllWebhooks**
> deleteAllWebhooks()

Delete all webhooks

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteWebhook"></a>
# **deleteWebhook**
> deleteWebhook(inboxId, webhookId)

Delete and disable a Webhook for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]
 **webhookId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteWebhookById"></a>
# **deleteWebhookById**
> deleteWebhookById(webhookId)

Delete a webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllWebhookResults"></a>
# **getAllWebhookResults**
> PageWebhookResult getAllWebhookResults(page, size, sort, searchFilter, since, before, unseenOnly)

Get results for all webhooks

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **unseenOnly** | **Boolean**| Filter for unseen exceptions only | [optional] [default to null]

### Return type

[**PageWebhookResult**](../Models/PageWebhookResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getAllWebhooks"></a>
# **getAllWebhooks**
> PageWebhookProjection getAllWebhooks(page, size, sort, searchFilter, since, before)

List Webhooks Paginated

    List webhooks in paginated form. Allows for page index, page size, and sort direction.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size for paginated result list. | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to DESC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageWebhookProjection**](../Models/PageWebhookProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getInboxWebhooksPaginated"></a>
# **getInboxWebhooksPaginated**
> PageWebhookProjection getInboxWebhooksPaginated(inboxId, page, size, sort, searchFilter, since, before)

Get paginated webhooks for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageWebhookProjection**](../Models/PageWebhookProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getJsonSchemaForWebhookPayload"></a>
# **getJsonSchemaForWebhookPayload**
> JSONSchemaDto getJsonSchemaForWebhookPayload(webhookId)



    Get JSON Schema definition for webhook payload

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**JSONSchemaDto**](../Models/JSONSchemaDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTestWebhookPayload"></a>
# **getTestWebhookPayload**
> AbstractWebhookPayload getTestWebhookPayload(eventName)



    Get test webhook payload example. Response content depends on eventName passed. Uses &#x60;EMAIL_RECEIVED&#x60; as default.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **eventName** | **String**|  | [optional] [default to null] [enum: EMAIL_RECEIVED, NEW_EMAIL, NEW_CONTACT, NEW_ATTACHMENT, EMAIL_OPENED, EMAIL_READ, BOUNCE, BOUNCE_RECIPIENT]

### Return type

[**AbstractWebhookPayload**](../Models/AbstractWebhookPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTestWebhookPayloadBounce"></a>
# **getTestWebhookPayloadBounce**
> WebhookBouncePayload getTestWebhookPayloadBounce()



    Get webhook test payload for bounce

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookBouncePayload**](../Models/WebhookBouncePayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTestWebhookPayloadBounceRecipient"></a>
# **getTestWebhookPayloadBounceRecipient**
> WebhookBounceRecipientPayload getTestWebhookPayloadBounceRecipient()



    Get webhook test payload for bounce recipient

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookBounceRecipientPayload**](../Models/WebhookBounceRecipientPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

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
- **Accept**: */*

<a name="getTestWebhookPayloadEmailRead"></a>
# **getTestWebhookPayloadEmailRead**
> WebhookEmailReadPayload getTestWebhookPayloadEmailRead()



    Get webhook test payload for email opened event

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookEmailReadPayload**](../Models/WebhookEmailReadPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTestWebhookPayloadForWebhook"></a>
# **getTestWebhookPayloadForWebhook**
> AbstractWebhookPayload getTestWebhookPayloadForWebhook(webhookId)



    Get example payload for webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**AbstractWebhookPayload**](../Models/AbstractWebhookPayload)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

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
- **Accept**: */*

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
- **Accept**: */*

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
- **Accept**: */*

<a name="getWebhook"></a>
# **getWebhook**
> WebhookDto getWebhook(webhookId)

Get a webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**WebhookDto**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getWebhookResult"></a>
# **getWebhookResult**
> WebhookResultDto getWebhookResult(webhookResultId)

Get a webhook result for a webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookResultId** | [**UUID**](../Models/)| Webhook Result ID | [default to null]

### Return type

[**WebhookResultDto**](../Models/WebhookResultDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getWebhookResults"></a>
# **getWebhookResults**
> PageWebhookResult getWebhookResults(webhookId, page, size, sort, searchFilter, since, before, unseenOnly)

Get a webhook results for a webhook

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)| ID of webhook to get results for | [default to null]
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **unseenOnly** | **Boolean**| Filter for unseen exceptions only | [optional] [default to null]

### Return type

[**PageWebhookResult**](../Models/PageWebhookResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getWebhookResultsUnseenErrorCount"></a>
# **getWebhookResultsUnseenErrorCount**
> UnseenErrorCountDto getWebhookResultsUnseenErrorCount(inboxId)

Get count of unseen webhook results with error status

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**UnseenErrorCountDto**](../Models/UnseenErrorCountDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getWebhooks"></a>
# **getWebhooks**
> List getWebhooks(inboxId)

Get all webhooks for an Inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**List**](../Models/WebhookDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="redriveWebhookResult"></a>
# **redriveWebhookResult**
> WebhookRedriveResult redriveWebhookResult(webhookResultId)

Get a webhook result and try to resend the original webhook payload

    Allows you to resend a webhook payload that was already sent. Webhooks that fail are retried automatically for 24 hours and then put in a dead letter queue. You can retry results manually using this method.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookResultId** | [**UUID**](../Models/)| Webhook Result ID | [default to null]

### Return type

[**WebhookRedriveResult**](../Models/WebhookRedriveResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="sendTestData"></a>
# **sendTestData**
> WebhookTestResult sendTestData(webhookId)

Send webhook test data

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhookId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**WebhookTestResult**](../Models/WebhookTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

