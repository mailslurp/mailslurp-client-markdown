# DomainControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDomain**](DomainControllerApi.md#createDomain) | **POST** /domains | Create Domain
[**deleteDomain**](DomainControllerApi.md#deleteDomain) | **DELETE** /domains/{id} | Delete a domain
[**getDomain**](DomainControllerApi.md#getDomain) | **GET** /domains/{id} | Get a domain
[**getDomains**](DomainControllerApi.md#getDomains) | **GET** /domains | Get domains


<a name="createDomain"></a>
# **createDomain**
> DomainDto createDomain(domainOptions)

Create Domain

    Link a domain that you own with MailSlurp so you can create email addresses using it. Endpoint returns DNS records used for validation. You must add these verification records to your host provider&#39;s DNS setup to verify the domain.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainOptions** | [**CreateDomainOptions**](..//Models/CreateDomainOptions.md)| domainOptions |

### Return type

[**DomainDto**](..//Models/DomainDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteDomain"></a>
# **deleteDomain**
> deleteDomain(id)

Delete a domain

    Delete a domain. This will disable any existing inboxes that use this domain.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](..//Models/.md)| id | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getDomain"></a>
# **getDomain**
> DomainDto getDomain(id)

Get a domain

    Returns domain verification status and tokens for a given domain

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](..//Models/.md)| id | [default to null]

### Return type

[**DomainDto**](..//Models/DomainDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getDomains"></a>
# **getDomains**
> List getDomains()

Get domains

    List all custom domains you have created

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](..//Models/DomainPreview.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

