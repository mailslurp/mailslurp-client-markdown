# AttachmentControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteAllAttachments**](AttachmentControllerApi#deleteAllAttachments) | **DELETE** /attachments | Delete all attachments
[**deleteAttachment**](AttachmentControllerApi#deleteAttachment) | **DELETE** /attachments/{attachmentId} | Delete an attachment
[**downloadAttachmentAsBase64Encoded**](AttachmentControllerApi#downloadAttachmentAsBase64Encoded) | **GET** /attachments/{attachmentId}/base64 | Get email attachment as base64 encoded string as alternative to binary responses. To read the content decode the Base64 encoded contents.
[**downloadAttachmentAsBytes**](AttachmentControllerApi#downloadAttachmentAsBytes) | **GET** /attachments/{attachmentId}/bytes | Download attachments. Get email attachment bytes. If you have trouble with byte responses try the &#x60;downloadAttachmentBase64&#x60; response endpoints.
[**getAttachment**](AttachmentControllerApi#getAttachment) | **GET** /attachments/{attachmentId} | Get an attachment entity
[**getAttachmentInfo**](AttachmentControllerApi#getAttachmentInfo) | **GET** /attachments/{attachmentId}/metadata | Get email attachment metadata information
[**getAttachments1**](AttachmentControllerApi#getAttachments1) | **GET** /attachments | Get email attachments
[**uploadAttachment**](AttachmentControllerApi#uploadAttachment) | **POST** /attachments | Upload an attachment for sending using base64 file encoding. Returns an array whose first element is the ID of the uploaded attachment.
[**uploadAttachmentBytes**](AttachmentControllerApi#uploadAttachmentBytes) | **POST** /attachments/bytes | Upload an attachment for sending using file byte stream input octet stream. Returns an array whose first element is the ID of the uploaded attachment.
[**uploadMultipartForm**](AttachmentControllerApi#uploadMultipartForm) | **POST** /attachments/multipart | Upload an attachment for sending using a Multipart Form request. Returns an array whose first element is the ID of the uploaded attachment.


<a name="deleteAllAttachments"></a>
# **deleteAllAttachments**
> deleteAllAttachments()

Delete all attachments

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteAttachment"></a>
# **deleteAttachment**
> deleteAttachment(attachmentId)

Delete an attachment

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="downloadAttachmentAsBase64Encoded"></a>
# **downloadAttachmentAsBase64Encoded**
> DownloadAttachmentDto downloadAttachmentAsBase64Encoded(attachmentId)

Get email attachment as base64 encoded string as alternative to binary responses. To read the content decode the Base64 encoded contents.

    Returns the specified attachment for a given email as a base 64 encoded string. The response type is application/json. This method is similar to the &#x60;downloadAttachment&#x60; method but allows some clients to get around issues with binary responses.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]

### Return type

[**DownloadAttachmentDto**](../Models/DownloadAttachmentDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="downloadAttachmentAsBytes"></a>
# **downloadAttachmentAsBytes**
> List downloadAttachmentAsBytes(attachmentId)

Download attachments. Get email attachment bytes. If you have trouble with byte responses try the &#x60;downloadAttachmentBase64&#x60; response endpoints.

    Returns the specified attachment for a given email as a stream / array of bytes. You can find attachment ids in email responses endpoint responses. The response type is application/octet-stream.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]

### Return type

[**List**](../Models/ByteArray)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream

<a name="getAttachment"></a>
# **getAttachment**
> AttachmentEntity getAttachment(attachmentId)

Get an attachment entity

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]

### Return type

[**AttachmentEntity**](../Models/AttachmentEntity)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getAttachmentInfo"></a>
# **getAttachmentInfo**
> AttachmentMetaData getAttachmentInfo(attachmentId)

Get email attachment metadata information

    Returns the metadata for an attachment. It is saved separately to the content of the attachment. Contains properties &#x60;name&#x60; and &#x60;content-type&#x60; and &#x60;content-length&#x60; in bytes for a given attachment.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]

### Return type

[**AttachmentMetaData**](../Models/AttachmentMetaData)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getAttachments1"></a>
# **getAttachments1**
> PageAttachmentEntity getAttachments1(page, size, sort, fileNameFilter, since, before)

Get email attachments

    Get all attachments in paginated response. Each entity contains meta data for the attachment such as &#x60;name&#x60; and &#x60;content-type&#x60;. Use the &#x60;attachmentId&#x60; and the download endpoints to get the file contents.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index event list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size event list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **fileNameFilter** | **String**| Optional file name and content type search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageAttachmentEntity**](../Models/PageAttachmentEntity)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="uploadAttachment"></a>
# **uploadAttachment**
> List uploadAttachment(UploadAttachmentOptions)

Upload an attachment for sending using base64 file encoding. Returns an array whose first element is the ID of the uploaded attachment.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UploadAttachmentOptions** | [**UploadAttachmentOptions**](../Models/UploadAttachmentOptions)|  |

### Return type

[**List**](../Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="uploadAttachmentBytes"></a>
# **uploadAttachmentBytes**
> List uploadAttachmentBytes(ByteArray, contentType, filename)

Upload an attachment for sending using file byte stream input octet stream. Returns an array whose first element is the ID of the uploaded attachment.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ByteArray** | [**List**](../Models/ByteArray)|  |
 **contentType** | **String**| Optional contentType for file. For instance &#x60;application/pdf&#x60; | [optional] [default to null]
 **filename** | **String**| Optional filename to save upload with | [optional] [default to null]

### Return type

[**List**](../Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/octet-stream
- **Accept**: application/json

<a name="uploadMultipartForm"></a>
# **uploadMultipartForm**
> List uploadMultipartForm(contentType, filename, x-filename, InlineObject)

Upload an attachment for sending using a Multipart Form request. Returns an array whose first element is the ID of the uploaded attachment.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contentType** | **String**| Optional content type of attachment | [optional] [default to null]
 **filename** | **String**| Optional name of file | [optional] [default to null]
 **x-filename** | **String**| Optional content type header of attachment | [optional] [default to null]
 **InlineObject** | [**InlineObject**](../Models/InlineObject)|  | [optional]

### Return type

[**List**](../Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

