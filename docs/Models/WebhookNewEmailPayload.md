# WebhookNewEmailPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | Id of the inbox that received an email | [default to null]
**emailId** | [**UUID**](UUID) | ID of the email that was received. Use this ID for fetching the email with the &#x60;EmailController&#x60;. | [default to null]
**createdAt** | [**Date**](DateTime) | Date time of event creation | [default to null]
**to** | [**List**](string) | List of &#x60;To&#x60; recipient email addresses that the email was addressed to. See recipients object for names. | [default to null]
**from** | [**String**](string) | Who the email was sent from. An email address - see fromName for the sender name. | [default to null]
**cc** | [**List**](string) | List of &#x60;CC&#x60; recipients email addresses that the email was addressed to. See recipients object for names. | [default to null]
**bcc** | [**List**](string) | List of &#x60;BCC&#x60; recipients email addresses that the email was addressed to. See recipients object for names. | [default to null]
**subject** | [**String**](string) | The subject line of the email message as specified by SMTP subject header | [optional] [default to null]
**attachmentMetaDatas** | [**List**](AttachmentMetaData) | List of attachment meta data objects if attachments present | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

