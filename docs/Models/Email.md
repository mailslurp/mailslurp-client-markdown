# Email
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**analysis** | [**EmailAnalysis**](EmailAnalysis) |  | [optional] [default to null]
**attachments** | [**List**](string) | List of IDs of attachments found in the email. Use these IDs with the Inbox and Email Controllers to download attachments and attachment meta data such as filesize, name, extension. | [optional] [default to null]
**bcc** | [**List**](string) | List of &#x60;BCC&#x60; recipients email was addressed to | [optional] [default to null]
**body** | [**String**](string) | The body of the email message | [optional] [default to null]
**bodyMD5Hash** | [**String**](string) | A hash signature of the email message | [optional] [default to null]
**cc** | [**List**](string) | List of &#x60;CC&#x60; recipients email was addressed to | [optional] [default to null]
**charset** | [**String**](string) | Detected character set of the email body such as UTF-8 | [optional] [default to null]
**createdAt** | [**Date**](DateTime) | When was the email received by MailSlurp | [optional] [default to null]
**from** | [**String**](string) | Who the email was sent from | [optional] [default to null]
**headers** | [**Map**](string) |  | [optional] [default to null]
**id** | [**UUID**](UUID) | ID of the email | [optional] [default to null]
**inboxId** | [**UUID**](UUID) | ID of the inbox that received the email | [optional] [default to null]
**isHTML** | [**Boolean**](boolean) | Was HTML sent in the email body | [optional] [default to null]
**read** | [**Boolean**](boolean) | Has the email been viewed ever. This means viewed in the dashboard or requested via the full email entity endpoints | [optional] [default to null]
**replyTo** | [**String**](string) | The replyTo field on the received email | [optional] [default to null]
**subject** | [**String**](string) | The subject line of the email message | [optional] [default to null]
**teamAccess** | [**Boolean**](boolean) | Can the email be accessed by organization team members | [optional] [default to null]
**to** | [**List**](string) | List of &#x60;To&#x60; recipients email was addressed to | [optional] [default to null]
**updatedAt** | [**Date**](DateTime) | When was the email last updated | [optional] [default to null]
**userId** | [**UUID**](UUID) | ID of user that email belongs | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

