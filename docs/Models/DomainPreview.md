# DomainPreview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID) |  | [optional] [default to null]
**domain** | [**String**](string) |  | [optional] [default to null]
**catchAllInboxId** | [**UUID**](UUID) |  | [optional] [default to null]
**createdAt** | [**Date**](DateTime) |  | [optional] [default to null]
**domainType** | [**String**](string) | Type of domain. Dictates type of inbox that can be created with domain. HTTP means inboxes are processed using SES while SMTP inboxes use a custom SMTP mail server. SMTP does not support sending so use HTTP for sending emails. | [optional] [default to null]
**verified** | [**Boolean**](boolean) |  | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

