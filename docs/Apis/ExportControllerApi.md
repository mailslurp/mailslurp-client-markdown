# ExportControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**exportEntities**](ExportControllerApi#exportEntities) | **GET** /export | Export inboxes link callable via browser
[**getExportLink**](ExportControllerApi#getExportLink) | **POST** /export | Get export link


<a name="exportEntities"></a>
# **exportEntities**
> byte[] exportEntities(apiKey, exportType, outputFormat, createdEarliestTime, createdOldestTime, excludePreviouslyExported, filter, listSeparatorToken)

Export inboxes link callable via browser

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apiKey** | **String**| apiKey | [default to null]
 **exportType** | **String**| exportType | [default to null] [enum: INBOXES, CONTACTS, ATTACHMENTS, EMAILS]
 **outputFormat** | **String**| outputFormat | [default to null] [enum: CSV_DEFAULT, CSV_EXCEL]
 **createdEarliestTime** | **Date**| createdEarliestTime | [optional] [default to null]
 **createdOldestTime** | **Date**| createdOldestTime | [optional] [default to null]
 **excludePreviouslyExported** | **Boolean**| excludePreviouslyExported | [optional] [default to null]
 **filter** | **String**| filter | [optional] [default to null]
 **listSeparatorToken** | **String**| listSeparatorToken | [optional] [default to null]

### Return type

[**byte[]**](../Models/ByteArray)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getExportLink"></a>
# **getExportLink**
> ExportLink getExportLink(exportType, exportOptions, apiKey)

Get export link

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exportType** | **String**| exportType | [default to null] [enum: INBOXES, CONTACTS, ATTACHMENTS, EMAILS]
 **exportOptions** | [**ExportOptions**](../Models/ExportOptions)| exportOptions |
 **apiKey** | **String**| apiKey | [optional] [default to null]

### Return type

[**ExportLink**](../Models/ExportLink)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

