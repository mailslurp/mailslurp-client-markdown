# SentEmailDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID) | ID of sent email | [default to null]
**userId** | [**UUID**](UUID) | User ID | [default to null]
**inboxId** | [**UUID**](UUID) | Inbox ID email was sent from | [default to null]
**to** | [**List**](string) | Recipients email was sent to | [optional] [default to null]
**from** | [**String**](string) |  | [optional] [default to null]
**replyTo** | [**String**](string) |  | [optional] [default to null]
**cc** | [**List**](string) |  | [optional] [default to null]
**bcc** | [**List**](string) |  | [optional] [default to null]
**attachments** | [**List**](string) | Array of IDs of attachments that were sent with this email | [optional] [default to null]
**subject** | [**String**](string) |  | [optional] [default to null]
**bodyMD5Hash** | [**String**](string) | MD5 Hash | [optional] [default to null]
**body** | [**String**](string) |  | [optional] [default to null]
**charset** | [**String**](string) |  | [optional] [default to null]
**isHTML** | [**Boolean**](boolean) |  | [optional] [default to null]
**sentAt** | [**Date**](DateTime) |  | [default to null]
**pixelIds** | [**List**](UUID) |  | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

