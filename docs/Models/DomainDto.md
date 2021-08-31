# DomainDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**catchAllInboxId** | [**UUID**](UUID) | The optional catch all inbox that will receive emails sent to the domain that cannot be matched. | [optional] [default to null]
**createdAt** | [**Date**](DateTime) |  | [default to null]
**dkimTokens** | [**List**](string) | Unique token DKIM tokens | [optional] [default to null]
**domain** | [**String**](string) | Custom domain name | [optional] [default to null]
**domainNameRecords** | [**List**](DomainNameRecord) | List of DNS domain name records (C, MX, TXT) etc that you must add to the DNS server associated with your domain provider. | [optional] [default to null]
**domainType** | [**String**](string) | The type of domain. SMTP or HTTP domains differ in what inboxes can be used with them. | [optional] [default to null]
**id** | [**UUID**](UUID) |  | [default to null]
**isVerified** | [**Boolean**](boolean) | Whether domain has been verified or not. If the domain is not verified after 72 hours there is most likely an issue with the domains DNS records. | [optional] [default to null]
**updatedAt** | [**Date**](DateTime) |  | [default to null]
**userId** | [**UUID**](UUID) |  | [default to null]
**verificationToken** | [**String**](string) | Verification tokens | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

