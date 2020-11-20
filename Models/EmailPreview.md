# EmailPreview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | [**List**](string.md) | List of IDs of attachments found in the email. Use these IDs with the Inbox and Email Controllers to download attachments and attachment meta data such as filesize, name, extension. | [optional] [default to null]
**bcc** | [**List**](string.md) | List of &#x60;BCC&#x60; recipients email was addressed to | [optional] [default to null]
**cc** | [**List**](string.md) | List of &#x60;CC&#x60; recipients email was addressed to | [optional] [default to null]
**createdAt** | [**Date**](DateTime.md) | When was the email received by MailSlurp | [optional] [default to null]
**from** | [**String**](string.md) | Who the email was sent from | [optional] [default to null]
**id** | [**UUID**](UUID.md) | ID of the email | [optional] [default to null]
**read** | [**Boolean**](boolean.md) | Has the email been viewed ever | [optional] [default to null]
**subject** | [**String**](string.md) | The subject line of the email message | [optional] [default to null]
**to** | [**List**](string.md) | List of &#x60;To&#x60; recipients email was addressed to | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

