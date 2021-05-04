# WebhookDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**basicAuth** | [**Boolean**](boolean) | Does webhook expect basic authentication? If true it means you created this webhook with a username and password. MailSlurp will use these in the URL to authenticate itself. | [optional] [default to null]
**createdAt** | [**Date**](DateTime) | When the webhook was created | [optional] [default to null]
**id** | [**UUID**](UUID) | ID of the Webhook | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | The inbox that the Webhook will be triggered by | [optional] [default to null]
**method** | [**String**](string) | HTTP method that your server endpoint must listen for | [optional] [default to null]
**name** | [**String**](string) | Name of the webhook | [optional] [default to null]
**payloadJsonSchema** | [**String**](string) | JSON Schema for the payload that will be sent to your URL via the HTTP method described. | [optional] [default to null]
**updatedAt** | [**Date**](DateTime) |  | [default to null]
**url** | [**String**](string) | URL of your server that the webhook will be sent to. The schema of the JSON that is sent is described by the payloadJsonSchema. | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

