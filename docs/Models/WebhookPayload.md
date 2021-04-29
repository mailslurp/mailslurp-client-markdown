# WebhookPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachmentMetaDatas** | [**List**](AttachmentMetaData) | List of attachment meta data objects if attachments present | [optional] [default to null]
**bcc** | [**List**](string) | List of &#x60;BCC&#x60; recipients email was addressed to | [optional] [default to null]
**cc** | [**List**](string) | List of &#x60;CC&#x60; recipients email was addressed to | [optional] [default to null]
**createdAt** | [**Date**](DateTime) | Date time of event creation | [optional] [default to null]
**emailId** | [**UUID**](UUID) | ID of the email that was received. Use this ID for fetching the email | [optional] [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for | [optional] [default to null]
**from** | [**String**](string) | Who the email was sent from | [optional] [default to null]
**id** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | Id of the inbox that receive an email | [optional] [default to null]
**subject** | [**String**](string) | The subject line of the email message | [optional] [default to null]
**to** | [**List**](string) | List of &#x60;To&#x60; recipients email was addressed to | [optional] [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [optional] [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

