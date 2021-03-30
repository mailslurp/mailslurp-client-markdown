# ReplyToEmailOptions
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | [**List**](string.md) | List of uploaded attachments to send with the reply. Optional. | [optional] [default to null]
**body** | [**String**](string.md) | Body of the reply email you want to send | [optional] [default to null]
**charset** | [**String**](string.md) | The charset that your message should be sent with. Optional. Default is UTF-8 | [optional] [default to null]
**from** | [**String**](string.md) | The from header that should be used. Optional | [optional] [default to null]
**isHTML** | [**Boolean**](boolean.md) | Is the reply HTML | [optional] [default to null]
**replyTo** | [**String**](string.md) | The replyTo header that should be used. Optional | [optional] [default to null]
**sendStrategy** | [**String**](string.md) | When to send the email. Typically immediately | [optional] [default to null]
**template** | [**UUID**](UUID.md) | Template ID to use instead of body. Will use template variable map to fill defined variable slots. | [optional] [default to null]
**templateVariables** | [**Object**](.md) | Template variables if using a template | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

