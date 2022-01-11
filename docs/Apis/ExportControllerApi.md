# ExportControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**exportEntities**](ExportControllerApi#exportEntities) | **GET** /export | Export inboxes link callable via browser
[**getExportLink**](ExportControllerApi#getExportLink) | **POST** /export | Get export link


<a name="exportEntities"></a>
# **exportEntities**
> List exportEntities(exportType, apiKey, outputFormat, filter, listSeparatorToken, excludePreviouslyExported, createdEarliestTime, createdOldestTime)

Export inboxes link callable via browser

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exportType** | **String**|  | [default to null] [enum: INBOXES, CONTACTS, ATTACHMENTS, EMAILS]
 **apiKey** | **String**|  | [default to null]
 **outputFormat** | **String**|  | [default to null] [enum: CSV_DEFAULT, CSV_EXCEL]
 **filter** | **String**|  | [optional] [default to null]
 **listSeparatorToken** | **String**|  | [optional] [default to null]
 **excludePreviouslyExported** | **Boolean**|  | [optional] [default to null]
 **createdEarliestTime** | **Date**|  | [optional] [default to null]
 **createdOldestTime** | **Date**|  | [optional] [default to null]

### Return type

[**List**](../Models/ByteArray)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getExportLink"></a>
# **getExportLink**
> ExportLink getExportLink(exportType, ExportOptions, apiKey)

Get export link

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **exportType** | **String**|  | [default to null] [enum: INBOXES, CONTACTS, ATTACHMENTS, EMAILS]
 **ExportOptions** | [**ExportOptions**](../Models/ExportOptions)|  |
 **apiKey** | **String**|  | [optional] [default to null]

### Return type

[**ExportLink**](../Models/ExportLink)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

