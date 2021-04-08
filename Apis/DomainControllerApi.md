# DomainControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addDomainWildcardCatchAll**](DomainControllerApi.md#addDomainWildcardCatchAll) | **POST** /domains/{id}/wildcard | Add catch all wild card inbox to domain
[**createDomain**](DomainControllerApi.md#createDomain) | **POST** /domains | Create Domain
[**deleteDomain**](DomainControllerApi.md#deleteDomain) | **DELETE** /domains/{id} | Delete a domain
[**getDomain**](DomainControllerApi.md#getDomain) | **GET** /domains/{id} | Get a domain
[**getDomains**](DomainControllerApi.md#getDomains) | **GET** /domains | Get domains
[**updateDomain**](DomainControllerApi.md#updateDomain) | **PUT** /domains/{id} | Update a domain


<a name="addDomainWildcardCatchAll"></a>
# **addDomainWildcardCatchAll**
> DomainDto addDomainWildcardCatchAll(id)

Add catch all wild card inbox to domain

    Add a catch all inbox to a domain so that any emails sent to it that cannot be matched will be sent to the catch all inbox generated

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
> List deleteDomain(id)

Delete a domain

    Delete a domain. This will disable any existing inboxes that use this domain.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](..//Models/.md)| id | [default to null]

### Return type

[**List**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

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

<a name="updateDomain"></a>
# **updateDomain**
> DomainDto updateDomain(id, updateDomainDto)

Update a domain

    Update values on a domain. Note you cannot change the domain name as it is immutable. Recreate the domain if you need to alter this.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](..//Models/.md)| id | [default to null]
 **updateDomainDto** | [**UpdateDomainOptions**](..//Models/UpdateDomainOptions.md)| updateDomainDto |

### Return type

[**DomainDto**](..//Models/DomainDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

