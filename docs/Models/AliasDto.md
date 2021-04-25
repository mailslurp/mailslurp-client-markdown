# AliasDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createdAt** | [**Date**](DateTime) |  | [optional] [default to null]
**emailAddress** | [**String**](string) | The alias&#39;s email address for receiving email | [optional] [default to null]
**id** | [**UUID**](UUID) |  | [default to null]
**inboxId** | [**UUID**](UUID) | Inbox that is associated with the alias | [optional] [default to null]
**isVerified** | [**Boolean**](boolean) | Has the alias been verified. You must verify an alias if the masked email address has not yet been verified by your account | [optional] [default to null]
**maskedEmailAddress** | [**String**](string) | The underlying email address that is hidden and will received forwarded email | [optional] [default to null]
**name** | [**String**](string) |  | [optional] [default to null]
**updatedAt** | [**Date**](DateTime) |  | [optional] [default to null]
**useThreads** | [**Boolean**](boolean) | If alias will generate response threads or not when email are received by it | [optional] [default to null]
**userId** | [**UUID**](UUID) |  | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

