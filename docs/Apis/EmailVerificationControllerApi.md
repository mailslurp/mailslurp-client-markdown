# EmailVerificationControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getValidationRequests**](EmailVerificationControllerApi#getValidationRequests) | **GET** /email-verification/validation-requests | Validate a list of email addresses. Per unit billing. See your plan for pricing.
[**validateEmailAddressList**](EmailVerificationControllerApi#validateEmailAddressList) | **POST** /email-verification/email-address-list | Validate a list of email addresses. Per unit billing. See your plan for pricing.


<a name="getValidationRequests"></a>
# **getValidationRequests**
> PageEmailValidationRequest getValidationRequests(page, size, sort, searchFilter, since, before, isValid)

Validate a list of email addresses. Per unit billing. See your plan for pricing.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size for paginated result list. | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to DESC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **isValid** | **Boolean**| Filter where email is valid is true or false | [optional] [default to null]

### Return type

[**PageEmailValidationRequest**](../Models/PageEmailValidationRequest)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="validateEmailAddressList"></a>
# **validateEmailAddressList**
> ValidateEmailAddressListResult validateEmailAddressList(ValidateEmailAddressListOptions)

Validate a list of email addresses. Per unit billing. See your plan for pricing.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ValidateEmailAddressListOptions** | [**ValidateEmailAddressListOptions**](../Models/ValidateEmailAddressListOptions)|  |

### Return type

[**ValidateEmailAddressListResult**](../Models/ValidateEmailAddressListResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

