# AliasControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAlias**](AliasControllerApi.md#createAlias) | **POST** /aliases | Create an email alias
[**createAnonymousAlias**](AliasControllerApi.md#createAnonymousAlias) | **POST** /aliases/anonymous | Create an anonymous email alias
[**deleteAlias**](AliasControllerApi.md#deleteAlias) | **DELETE** /aliases/{aliasId} | Delete an owned alias
[**getAlias**](AliasControllerApi.md#getAlias) | **GET** /aliases/{aliasId} | Get an email alias
[**getAliases**](AliasControllerApi.md#getAliases) | **GET** /aliases | Get all email aliases
[**updateAlias**](AliasControllerApi.md#updateAlias) | **PUT** /aliases/{aliasId} | Update an owned alias


<a name="createAlias"></a>
# **createAlias**
> createAlias(createOwnedAliasOptions)

Create an email alias

    Create an email alias belonging to a user ID. To create anonymous aliases use the &#x60;createAnonymousAlias&#x60; method.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createOwnedAliasOptions** | [**CreateOwnedAliasOptions**](..//Models/CreateOwnedAliasOptions.md)| createOwnedAliasOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="createAnonymousAlias"></a>
# **createAnonymousAlias**
> Alias createAnonymousAlias(createAnonymousAliasOptions)

Create an anonymous email alias

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAnonymousAliasOptions** | [**CreateAnonymousAliasOptions**](..//Models/CreateAnonymousAliasOptions.md)| createAnonymousAliasOptions |

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

Delete an owned alias

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
> Alias getAlias(aliasId)

Get an email alias

    Get an email alias by ID

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](..//Models/.md)| aliasId | [default to null]

### Return type

[**Alias**](..//Models/Alias.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAliases"></a>
# **getAliases**
> Page_Alias_ getAliases(page, size, sort)

Get all email aliases

    Get all email aliases in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in alias list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in alias list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**Page_Alias_**](..//Models/Page_Alias_.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="updateAlias"></a>
# **updateAlias**
> updateAlias(aliasId, createOwnedAliasOptions)

Update an owned alias

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](..//Models/.md)| aliasId | [default to null]
 **createOwnedAliasOptions** | [**CreateOwnedAliasOptions**](..//Models/CreateOwnedAliasOptions.md)| createOwnedAliasOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

