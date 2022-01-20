# WebhookNewAttachmentPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [default to null]
**attachmentId** | [**String**](string) | ID of attachment. Use the &#x60;AttachmentController&#x60; to | [default to null]
**name** | [**String**](string) | Filename of the attachment if present | [default to null]
**contentType** | [**String**](string) | Content type of attachment such as &#39;image/png&#39; or &#39;application/pdf | [default to null]
**contentLength** | [**Long**](long) | Size of attachment in bytes | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

