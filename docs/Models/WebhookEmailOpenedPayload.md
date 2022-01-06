# WebhookEmailOpenedPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [optional] [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [optional] [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [optional] [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | Id of the inbox that received an email | [optional] [default to null]
**pixelId** | [**UUID**](UUID) | ID of the tracking pixel | [optional] [default to null]
**sentEmailId** | [**UUID**](UUID) | ID of sent email | [optional] [default to null]
**recipient** | [**String**](string) | Email address for the recipient of the tracking pixel | [optional] [default to null]
**createdAt** | [**Date**](DateTime) | Date time of event creation | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

