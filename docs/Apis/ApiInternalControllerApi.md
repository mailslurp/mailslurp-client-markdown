# ApiInternalControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSamlUserOrCreate**](ApiInternalControllerApi#getSamlUserOrCreate) | **POST** /internal/saml/user | 


<a name="getSamlUserOrCreate"></a>
# **getSamlUserOrCreate**
> UserDto getSamlUserOrCreate(key, GetOrCreateSamlUserOptions)



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **String**|  | [default to null]
 **GetOrCreateSamlUserOptions** | [**GetOrCreateSamlUserOptions**](../Models/GetOrCreateSamlUserOptions)|  |

### Return type

[**UserDto**](../Models/UserDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

