# MailServerControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**describeMailServerDomain**](MailServerControllerApi#describeMailServerDomain) | **POST** /mail-server/describe/domain | Get DNS Mail Server records for a domain
[**getDnsLookup**](MailServerControllerApi#getDnsLookup) | **POST** /mail-server/describe/dns-lookup | Lookup DNS records for a domain
[**getIpAddress**](MailServerControllerApi#getIpAddress) | **POST** /mail-server/describe/ip-address | Get IP address for a domain
[**verifyEmailAddress**](MailServerControllerApi#verifyEmailAddress) | **POST** /mail-server/verify/email-address | Verify the existence of an email address at a given mail server.


<a name="describeMailServerDomain"></a>
# **describeMailServerDomain**
> DescribeMailServerDomainResult describeMailServerDomain(DescribeDomainOptions)

Get DNS Mail Server records for a domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DescribeDomainOptions** | [**DescribeDomainOptions**](../Models/DescribeDomainOptions)|  |

### Return type

[**DescribeMailServerDomainResult**](../Models/DescribeMailServerDomainResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="getDnsLookup"></a>
# **getDnsLookup**
> DNSLookupResults getDnsLookup(DNSLookupOptions)

Lookup DNS records for a domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DNSLookupOptions** | [**DNSLookupOptions**](../Models/DNSLookupOptions)|  |

### Return type

[**DNSLookupResults**](../Models/DNSLookupResults)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="getIpAddress"></a>
# **getIpAddress**
> IPAddressResult getIpAddress(name)

Get IP address for a domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**|  | [default to null]

### Return type

[**IPAddressResult**](../Models/IPAddressResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="verifyEmailAddress"></a>
# **verifyEmailAddress**
> EmailVerificationResult verifyEmailAddress(VerifyEmailAddressOptions)

Verify the existence of an email address at a given mail server.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VerifyEmailAddressOptions** | [**VerifyEmailAddressOptions**](../Models/VerifyEmailAddressOptions)|  |

### Return type

[**EmailVerificationResult**](../Models/EmailVerificationResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

