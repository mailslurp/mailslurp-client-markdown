# AliasControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAlias**](AliasControllerApi.md#createAlias) | **POST** /aliases | Create an email alias. Must be verified by clicking link inside verification email that will be sent to the address. Once verified the alias will be active.
[**deleteAlias**](AliasControllerApi.md#deleteAlias) | **DELETE** /aliases/{aliasId} | Delete an email alias
[**getAlias**](AliasControllerApi.md#getAlias) | **GET** /aliases/{aliasId} | Get an email alias
[**getAliasVerification**](AliasControllerApi.md#getAliasVerification) | **GET** /aliases/{aliasId}/verification | Get validation result from alias verification
[**getAliases**](AliasControllerApi.md#getAliases) | **GET** /aliases | Get all email aliases you have created
[**updateAlias**](AliasControllerApi.md#updateAlias) | **PUT** /aliases/{aliasId} | Update an email alias


<a name="createAlias"></a>
# **createAlias**
> Alias createAlias(createAliasOptions)

Create an email alias. Must be verified by clicking link inside verification email that will be sent to the address. Once verified the alias will be active.

    Email aliases use a MailSlurp randomly generated email address (or a custom domain inbox that you provide) to mask or proxy a real email address. Emails sent to the alias address will be forwarded to the hidden email address it was created for. If you want to send a reply use the threadId attached

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAliasOptions** | [**CreateAliasOptions**](..//Models/CreateAliasOptions.md)| createAliasOptions |

### Return type

[**Alias**](..//Models/Alias.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteAlias"></a>
# **deleteAlias**
> deleteAlias(aliasId)

Delete an email alias

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](..//Models/.md)| aliasId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAlias"></a>
# **getAlias**
> AliasDto getAlias(aliasId)

Get an email alias

    Get an email alias by ID

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](..//Models/.md)| aliasId | [default to null]

### Return type

[**AliasDto**](..//Models/AliasDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAliasVerification"></a>
# **getAliasVerification**
> AliasVerificationResult getAliasVerification(aliasId, emailAddress, verificationToken)

Get validation result from alias verification

    Verify an email alias email address with the verification token that was emailed to the address

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](..//Models/.md)| aliasId | [default to null]
 **emailAddress** | **String**| emailAddress | [default to null]
 **verificationToken** | **String**| verificationToken | [default to null]

### Return type

[**AliasVerificationResult**](..//Models/AliasVerificationResult.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAliases"></a>
# **getAliases**
> PageAlias getAliases(page, size, sort)

Get all email aliases you have created

    Get all email aliases in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in alias list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in alias list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageAlias**](..//Models/PageAlias.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="updateAlias"></a>
# **updateAlias**
> updateAlias(aliasId, updateAliasOptions)

Update an email alias

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](..//Models/.md)| aliasId | [default to null]
 **updateAliasOptions** | [**UpdateAliasOptions**](..//Models/UpdateAliasOptions.md)| updateAliasOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

