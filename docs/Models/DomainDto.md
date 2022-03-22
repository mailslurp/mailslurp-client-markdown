# DomainDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID) |  | [default to null]
**userId** | [**UUID**](UUID) |  | [default to null]
**domain** | [**String**](string) | Custom domain name | [default to null]
**verificationToken** | [**String**](string) | Verification tokens | [default to null]
**dkimTokens** | [**List**](string) | Unique token DKIM tokens | [default to null]
**isVerified** | [**Boolean**](boolean) | Whether domain has been verified or not. If the domain is not verified after 72 hours there is most likely an issue with the domains DNS records. | [default to null]
**domainNameRecords** | [**List**](DomainNameRecord) | List of DNS domain name records (C, MX, TXT) etc that you must add to the DNS server associated with your domain provider. | [default to null]
**catchAllInboxId** | [**UUID**](UUID) | The optional catch all inbox that will receive emails sent to the domain that cannot be matched. | [optional] [default to null]
**createdAt** | [**Date**](DateTime) |  | [default to null]
**updatedAt** | [**Date**](DateTime) |  | [default to null]
**domainType** | [**String**](string) | Type of domain. Dictates type of inbox that can be created with domain. HTTP means inboxes are processed using SES while SMTP inboxes use a custom SMTP mail server. SMTP does not support sending so use HTTP for sending emails. | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

