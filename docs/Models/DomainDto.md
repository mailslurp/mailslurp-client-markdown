# DomainDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID) |  | [optional] [default to null]
**userId** | [**UUID**](UUID) |  | [optional] [default to null]
**domain** | [**String**](string) | Custom domain name | [optional] [default to null]
**verificationToken** | [**String**](string) | Verification tokens | [optional] [default to null]
**dkimTokens** | [**List**](string) | Unique token DKIM tokens | [optional] [default to null]
**domainNameRecords** | [**List**](DomainNameRecord) | List of DNS domain name records (C, MX, TXT) etc that you must add to the DNS server associated with your domain provider. | [optional] [default to null]
**catchAllInboxId** | [**UUID**](UUID) | The optional catch all inbox that will receive emails sent to the domain that cannot be matched. | [optional] [default to null]
**createdAt** | [**Date**](DateTime) |  | [optional] [default to null]
**updatedAt** | [**Date**](DateTime) |  | [optional] [default to null]
**domainType** | [**String**](string) | Type of domain. Dictates type of inbox that can be created with domain. HTTP means inboxes are processed using SES while SMTP inboxes use a custom SMTP mail server. SMTP does not support sending so use HTTP for sending emails. | [optional] [default to null]
**verified** | [**Boolean**](boolean) |  | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

