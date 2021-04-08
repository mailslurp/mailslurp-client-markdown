# SentEmailsControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSentEmail**](SentEmailsControllerApi.md#getSentEmail) | **GET** /sent/{id} | Get sent email receipt
[**getSentEmails**](SentEmailsControllerApi.md#getSentEmails) | **GET** /sent | Get all sent emails in paginated form
[**getSentOrganizationEmails**](SentEmailsControllerApi.md#getSentOrganizationEmails) | **GET** /sent/organization | Get all sent organization emails in paginated form


<a name="getSentEmail"></a>
# **getSentEmail**
> SentEmailDto getSentEmail(id)

Get sent email receipt

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](..//Models/.md)| id | [default to null]

### Return type

[**SentEmailDto**](..//Models/SentEmailDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getSentEmails"></a>
# **getSentEmails**
> PageSentEmailProjection getSentEmails(inboxId, page, size, sort)

Get all sent emails in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| Optional inboxId to filter sender of sent emails by | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox sent email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageSentEmailProjection**](..//Models/PageSentEmailProjection.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getSentOrganizationEmails"></a>
# **getSentOrganizationEmails**
> PageSentEmailProjection getSentOrganizationEmails(inboxId, page, size, sort)

Get all sent organization emails in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| Optional inboxId to filter sender of sent emails by | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox sent email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageSentEmailProjection**](..//Models/PageSentEmailProjection.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

