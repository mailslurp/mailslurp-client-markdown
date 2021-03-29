# AliasDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createdAt** | [**Date**](DateTime.md) |  | [optional] [default to null]
**emailAddress** | [**String**](string.md) | The alias&#39;s email address for receiving email | [optional] [default to null]
**id** | [**UUID**](UUID.md) |  | [default to null]
**inboxId** | [**UUID**](UUID.md) | Inbox that is associated with the alias | [optional] [default to null]
**isVerified** | [**Boolean**](boolean.md) | Has the alias been verified. You must verify an alias if the masked email address has not yet been verified by your account | [optional] [default to null]
**maskedEmailAddress** | [**String**](string.md) | The underlying email address that is hidden and will received forwarded email | [optional] [default to null]
**name** | [**String**](string.md) |  | [optional] [default to null]
**updatedAt** | [**Date**](DateTime.md) |  | [optional] [default to null]
**useThreads** | [**Boolean**](boolean.md) | If alias will generate response threads or not when email are received by it | [optional] [default to null]
**userId** | [**UUID**](UUID.md) |  | [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

