# WebhookEmailOpenedPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | Id of the inbox that received an email | [default to null]
**pixelId** | [**UUID**](UUID) | ID of the tracking pixel | [default to null]
**sentEmailId** | [**UUID**](UUID) | ID of sent email | [default to null]
**recipient** | [**String**](string) | Email address for the recipient of the tracking pixel | [default to null]
**createdAt** | [**Date**](DateTime) | Date time of event creation | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

