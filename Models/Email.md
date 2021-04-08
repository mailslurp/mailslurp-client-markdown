# Email
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**analysis** | [**EmailAnalysis**](EmailAnalysis.md) |  | [optional] [default to null]
**attachments** | [**List**](string.md) | List of IDs of attachments found in the email. Use these IDs with the Inbox and Email Controllers to download attachments and attachment meta data such as filesize, name, extension. | [optional] [default to null]
**bcc** | [**List**](string.md) | List of &#x60;BCC&#x60; recipients email was addressed to | [optional] [default to null]
**body** | [**String**](string.md) | The body of the email message | [optional] [default to null]
**bodyMD5Hash** | [**String**](string.md) | A hash signature of the email message | [optional] [default to null]
**cc** | [**List**](string.md) | List of &#x60;CC&#x60; recipients email was addressed to | [optional] [default to null]
**charset** | [**String**](string.md) | Detected character set of the email body such as UTF-8 | [optional] [default to null]
**createdAt** | [**Date**](DateTime.md) | When was the email received by MailSlurp | [optional] [default to null]
**from** | [**String**](string.md) | Who the email was sent from | [optional] [default to null]
**headers** | [**Map**](string.md) |  | [optional] [default to null]
**id** | [**UUID**](UUID.md) | ID of the email | [optional] [default to null]
**inboxId** | [**UUID**](UUID.md) | ID of the inbox that received the email | [optional] [default to null]
**isHTML** | [**Boolean**](boolean.md) | Was HTML sent in the email body | [optional] [default to null]
**read** | [**Boolean**](boolean.md) | Has the email been viewed ever. This means viewed in the dashboard or requested via the full email entity endpoints | [optional] [default to null]
**replyTo** | [**String**](string.md) | The replyTo field on the received email | [optional] [default to null]
**subject** | [**String**](string.md) | The subject line of the email message | [optional] [default to null]
**teamAccess** | [**Boolean**](boolean.md) | Can the email be accessed by organization team members | [optional] [default to null]
**to** | [**List**](string.md) | List of &#x60;To&#x60; recipients email was addressed to | [optional] [default to null]
**updatedAt** | [**Date**](DateTime.md) | When was the email last updated | [optional] [default to null]
**userId** | [**UUID**](UUID.md) | ID of user that email belongs | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

