# Email
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID) | ID of the email entity | [default to null]
**userId** | [**UUID**](UUID) | ID of user that email belongs to | [default to null]
**inboxId** | [**UUID**](UUID) | ID of the inbox that received the email | [default to null]
**to** | [**List**](string) | List of &#x60;To&#x60; recipient email addresses that the email was addressed to. See recipients object for names. | [default to null]
**from** | [**String**](string) | Who the email was sent from. An email address - see fromName for the sender name. | [optional] [default to null]
**sender** | [**Sender**](Sender) |  | [optional] [default to null]
**recipients** | [**EmailRecipients**](EmailRecipients) |  | [optional] [default to null]
**replyTo** | [**String**](string) | The &#x60;replyTo&#x60; field on the received email message | [optional] [default to null]
**cc** | [**List**](string) | List of &#x60;CC&#x60; recipients email addresses that the email was addressed to. See recipients object for names. | [optional] [default to null]
**bcc** | [**List**](string) | List of &#x60;BCC&#x60; recipients email addresses that the email was addressed to. See recipients object for names. | [optional] [default to null]
**headers** | [**Map**](string) | Collection of SMTP headers attached to email | [optional] [default to null]
**attachments** | [**List**](string) | List of IDs of attachments found in the email. Use these IDs with the Inbox and Email Controllers to download attachments and attachment meta data such as filesize, name, extension. | [optional] [default to null]
**subject** | [**String**](string) | The subject line of the email message as specified by SMTP subject header | [optional] [default to null]
**body** | [**String**](string) | The body of the email message as text parsed from the SMTP message body (does not include attachments). Fetch the raw content to access the SMTP message and use the attachments property to access attachments. The body is stored separately to the email entity so the body is not returned in paginated results only in full single email or wait requests. | [optional] [default to null]
**bodyExcerpt** | [**String**](string) | An excerpt of the body of the email message for quick preview . | [optional] [default to null]
**bodyMD5Hash** | [**String**](string) | A hash signature of the email message using MD5. Useful for comparing emails without fetching full body. | [optional] [default to null]
**isHTML** | [**Boolean**](boolean) | Is the email body content type HTML? | [optional] [default to null]
**charset** | [**String**](string) | Detected character set of the email body such as UTF-8 | [optional] [default to null]
**analysis** | [**EmailAnalysis**](EmailAnalysis) |  | [optional] [default to null]
**createdAt** | [**Date**](DateTime) | When was the email received by MailSlurp | [default to null]
**updatedAt** | [**Date**](DateTime) | When was the email last updated | [default to null]
**read** | [**Boolean**](boolean) | Read flag. Has the email ever been viewed in the dashboard or fetched via the API with a hydrated body? If so the email is marked as read. Paginated results do not affect read status. Read status is different to email opened event as it depends on your own account accessing the email. Email opened is determined by tracking pixels sent to other uses if enable during sending. You can listened for both email read and email opened events using webhooks. | [default to null]
**teamAccess** | [**Boolean**](boolean) | Can the email be accessed by organization team members | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

