# SentEmailsControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteAllSentEmails**](SentEmailsControllerApi#deleteAllSentEmails) | **DELETE** /sent | Delete all sent email receipts
[**deleteSentEmail**](SentEmailsControllerApi#deleteSentEmail) | **DELETE** /sent/{id} | Delete sent email receipt
[**getAllSentTrackingPixels**](SentEmailsControllerApi#getAllSentTrackingPixels) | **GET** /sent/tracking-pixels | 
[**getRawSentEmailContents**](SentEmailsControllerApi#getRawSentEmailContents) | **GET** /sent/{emailId}/raw | Get raw sent email string. Returns unparsed raw SMTP message with headers and body.
[**getRawSentEmailJson**](SentEmailsControllerApi#getRawSentEmailJson) | **GET** /sent/{emailId}/raw/json | Get raw sent email in JSON. Unparsed SMTP message in JSON wrapper format.
[**getSentEmail**](SentEmailsControllerApi#getSentEmail) | **GET** /sent/{id} | Get sent email receipt
[**getSentEmailHTMLContent**](SentEmailsControllerApi#getSentEmailHTMLContent) | **GET** /sent/{id}/html | Get sent email HTML content
[**getSentEmailPreviewURLs**](SentEmailsControllerApi#getSentEmailPreviewURLs) | **GET** /sent/{id}/urls | Get sent email URL for viewing in browser or downloading
[**getSentEmailTrackingPixels**](SentEmailsControllerApi#getSentEmailTrackingPixels) | **GET** /sent/{id}/tracking-pixels | 
[**getSentEmails**](SentEmailsControllerApi#getSentEmails) | **GET** /sent | Get all sent emails in paginated form
[**getSentOrganizationEmails**](SentEmailsControllerApi#getSentOrganizationEmails) | **GET** /sent/organization | 


<a name="deleteAllSentEmails"></a>
# **deleteAllSentEmails**
> deleteAllSentEmails()

Delete all sent email receipts

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteSentEmail"></a>
# **deleteSentEmail**
> deleteSentEmail(id)

Delete sent email receipt

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllSentTrackingPixels"></a>
# **getAllSentTrackingPixels**
> PageTrackingPixelProjection getAllSentTrackingPixels(page, size, sort, searchFilter, since, before)



    Get all sent email tracking pixels in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in sent email tracking pixel list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in sent email tracking pixel list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageTrackingPixelProjection**](../Models/PageTrackingPixelProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getRawSentEmailContents"></a>
# **getRawSentEmailContents**
> String getRawSentEmailContents(emailId)

Get raw sent email string. Returns unparsed raw SMTP message with headers and body.

    Returns a raw, unparsed, and unprocessed sent email. If your client has issues processing the response it is likely due to the response content-type which is text/plain. If you need a JSON response content-type use the getRawSentEmailJson endpoint

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](../Models/)| ID of email | [default to null]

### Return type

[**String**](../Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain

<a name="getRawSentEmailJson"></a>
# **getRawSentEmailJson**
> RawEmailJson getRawSentEmailJson(emailId)

Get raw sent email in JSON. Unparsed SMTP message in JSON wrapper format.

    Returns a raw, unparsed, and unprocessed sent email wrapped in a JSON response object for easier handling when compared with the getRawSentEmail text/plain response

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](../Models/)| ID of email | [default to null]

### Return type

[**RawEmailJson**](../Models/RawEmailJson)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getSentEmail"></a>
# **getSentEmail**
> SentEmailDto getSentEmail(id)

Get sent email receipt

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**SentEmailDto**](../Models/SentEmailDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getSentEmailHTMLContent"></a>
# **getSentEmailHTMLContent**
> String getSentEmailHTMLContent(id)

Get sent email HTML content

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**String**](../Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/html

<a name="getSentEmailPreviewURLs"></a>
# **getSentEmailPreviewURLs**
> EmailPreviewUrls getSentEmailPreviewURLs(id)

Get sent email URL for viewing in browser or downloading

    Get a list of URLs for sent email content as text/html or raw SMTP message for viewing the message in a browser.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**EmailPreviewUrls**](../Models/EmailPreviewUrls)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getSentEmailTrackingPixels"></a>
# **getSentEmailTrackingPixels**
> PageTrackingPixelProjection getSentEmailTrackingPixels(id, page, size, sort, searchFilter, since, before)



    Get all tracking pixels for a sent email in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)|  | [default to null]
 **page** | **Integer**| Optional page index in sent email tracking pixel list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in sent email tracking pixel list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageTrackingPixelProjection**](../Models/PageTrackingPixelProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getSentEmails"></a>
# **getSentEmails**
> PageSentEmailProjection getSentEmails(inboxId, page, size, sort, searchFilter, since, before)

Get all sent emails in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inboxId to filter sender of sent emails by | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox sent email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageSentEmailProjection**](../Models/PageSentEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getSentOrganizationEmails"></a>
# **getSentOrganizationEmails**
> PageSentEmailProjection getSentOrganizationEmails(inboxId, page, size, sort, searchFilter, since, before)



    Get all sent organization emails in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inboxId to filter sender of sent emails by | [optional] [default to null]
 **page** | **Integer**| Optional page index in sent email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageSentEmailProjection**](../Models/PageSentEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

