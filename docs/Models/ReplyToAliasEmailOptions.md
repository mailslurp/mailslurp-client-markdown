# ReplyToAliasEmailOptions
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | [**String**](string) | Body of the reply email you want to send | [default to null]
**isHTML** | [**Boolean**](boolean) | Is the reply HTML | [default to null]
**charset** | [**String**](string) | The charset that your message should be sent with. Optional. Default is UTF-8 | [optional] [default to null]
**attachments** | [**List**](string) | List of uploaded attachments to send with the reply. Optional. | [optional] [default to null]
**templateVariables** | [**Map**](object) | Template variables if using a template | [optional] [default to null]
**template** | [**UUID**](UUID) | Template ID to use instead of body. Will use template variable map to fill defined variable slots. | [optional] [default to null]
**sendStrategy** | [**String**](string) | How an email should be sent based on its recipients | [optional] [default to null]
**useInboxName** | [**Boolean**](boolean) | Optionally use inbox name as display name for sender email address | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

