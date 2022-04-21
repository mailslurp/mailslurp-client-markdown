# WebhookDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID) | ID of the Webhook | [default to null]
**userId** | [**UUID**](UUID) | User ID of the Webhook | [default to null]
**basicAuth** | [**Boolean**](boolean) | Does webhook expect basic authentication? If true it means you created this webhook with a username and password. MailSlurp will use these in the URL to authenticate itself. | [default to null]
**name** | [**String**](string) | Name of the webhook | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | The inbox that the Webhook will be triggered by. If null then webhook triggered at account level | [optional] [default to null]
**url** | [**String**](string) | URL of your server that the webhook will be sent to. The schema of the JSON that is sent is described by the payloadJsonSchema. | [default to null]
**method** | [**String**](string) | HTTP method that your server endpoint must listen for | [default to null]
**payloadJsonSchema** | [**String**](string) | Deprecated. Fetch JSON Schema for webhook using the getJsonSchemaForWebhookPayload method | [default to null]
**createdAt** | [**Date**](DateTime) | When the webhook was created | [default to null]
**updatedAt** | [**Date**](DateTime) |  | [default to null]
**eventName** | [**String**](string) |  | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

