# WebhookEmailReadPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createdAt** | [**Date**](DateTime) | Date time of event creation | [optional] [default to null]
**emailId** | [**UUID**](UUID) | ID of the email that was received. Use this ID for fetching the email with the &#x60;EmailController&#x60;. | [optional] [default to null]
**emailIsRead** | [**Boolean**](boolean) | Is the email read | [optional] [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | Id of the inbox that received an email | [optional] [default to null]
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [optional] [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [optional] [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)
