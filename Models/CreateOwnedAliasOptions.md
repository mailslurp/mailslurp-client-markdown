# CreateOwnedAliasOptions
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emailAddress** | [**String**](string.md) | Email address to be hidden behind alias | [optional] [default to null]
**inboxId** | [**UUID**](UUID.md) | Optional inbox ID to attach to alias. Emails received by this inbox will be forwarded to the alias email address | [optional] [default to null]
**name** | [**String**](string.md) | Optional name for alias | [optional] [default to null]
**proxied** | [**Boolean**](boolean.md) | Optional proxied flag. When proxied is true alias will forward the incoming emails to the aliased email address via a proxy inbox. A new proxy is created for every new email thread. By replying to the proxy you can correspond with using your email alias without revealing your real email address. | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

