# DomainDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createdAt** | [**Date**](DateTime.md) |  | [default to null]
**dkimTokens** | [**List**](string.md) | Unique token DKIM tokens | [optional] [default to null]
**domain** | [**String**](string.md) | Custom domain name | [optional] [default to null]
**domainNameRecords** | [**List**](DomainNameRecord.md) | List of DNS domain name records (C, MX, TXT) etc that you must add to the DNS server associated with your domain provider. | [optional] [default to null]
**id** | [**UUID**](UUID.md) |  | [default to null]
**isVerified** | [**Boolean**](boolean.md) | Whether domain has been verified or not. If the domain is not verified after 72 hours there is most likely an issue with the domains DNS records. | [optional] [default to null]
**updatedAt** | [**Date**](DateTime.md) |  | [default to null]
**userId** | [**UUID**](UUID.md) |  | [default to null]
**verificationToken** | [**String**](string.md) | Verification tokens | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

