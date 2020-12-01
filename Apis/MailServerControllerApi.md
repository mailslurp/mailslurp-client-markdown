# MailServerControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**describeMailServerDomain**](MailServerControllerApi.md#describeMailServerDomain) | **POST** /mail-server/describe/domain | Get DNS Mail Server records for a domain
[**getDnsLookup**](MailServerControllerApi.md#getDnsLookup) | **POST** /mail-server/describe/dns-lookup | Lookup DNS records for a domain
[**getIpAddress**](MailServerControllerApi.md#getIpAddress) | **POST** /mail-server/describe/ip-address | Get IP address for a domain
[**verifyEmailAddress**](MailServerControllerApi.md#verifyEmailAddress) | **POST** /mail-server/verify/email-address | Verify the existence of an email address at a given mail server.


<a name="describeMailServerDomain"></a>
# **describeMailServerDomain**
> DescribeMailServerDomainResult describeMailServerDomain(describeOptions)

Get DNS Mail Server records for a domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **describeOptions** | [**DescribeDomainOptions**](..//Models/DescribeDomainOptions.md)| describeOptions |

### Return type

[**DescribeMailServerDomainResult**](..//Models/DescribeMailServerDomainResult.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="getDnsLookup"></a>
# **getDnsLookup**
> DNSLookupResults getDnsLookup(dnsLookupOptions)

Lookup DNS records for a domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dnsLookupOptions** | [**DNSLookupOptions**](..//Models/DNSLookupOptions.md)| dnsLookupOptions |

### Return type

[**DNSLookupResults**](..//Models/DNSLookupResults.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="getIpAddress"></a>
# **getIpAddress**
> IPAddressResult getIpAddress(name)

Get IP address for a domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name | [default to null]

### Return type

[**IPAddressResult**](..//Models/IPAddressResult.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="verifyEmailAddress"></a>
# **verifyEmailAddress**
> EmailVerificationResult verifyEmailAddress(verifyOptions)

Verify the existence of an email address at a given mail server.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verifyOptions** | [**VerifyEmailAddressOptions**](..//Models/VerifyEmailAddressOptions.md)| verifyOptions |

### Return type

[**EmailVerificationResult**](..//Models/EmailVerificationResult.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

