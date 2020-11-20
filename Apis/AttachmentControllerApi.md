# AttachmentControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**uploadAttachment**](AttachmentControllerApi.md#uploadAttachment) | **POST** /attachments | Upload an attachment for sending using base64 file encoding
[**uploadAttachmentBytes**](AttachmentControllerApi.md#uploadAttachmentBytes) | **POST** /attachments/bytes | Upload an attachment for sending using file byte stream input octet stream
[**uploadMultipartForm**](AttachmentControllerApi.md#uploadMultipartForm) | **POST** /attachments/multipart | Upload an attachment for sending using Multipart Form


<a name="uploadAttachment"></a>
# **uploadAttachment**
> List uploadAttachment(uploadOptions)

Upload an attachment for sending using base64 file encoding

    When sending emails with attachments first upload each attachment with this endpoint. Record the returned attachment IDs. Then use these attachment IDs in the SendEmailOptions when sending an email. This means that attachments can easily be reused.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uploadOptions** | [**UploadAttachmentOptions**](..//Models/UploadAttachmentOptions.md)| uploadOptions |

### Return type

[**List**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="uploadAttachmentBytes"></a>
# **uploadAttachmentBytes**
> List uploadAttachmentBytes(filename)

Upload an attachment for sending using file byte stream input octet stream

    When sending emails with attachments first upload each attachment with this endpoint. Record the returned attachment IDs. Then use these attachment IDs in the SendEmailOptions when sending an email. This means that attachments can easily be reused.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filename** | **String**| Optional filename to save upload with | [optional]

### Return type

[**List**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/octet-stream
- **Accept**: application/json

<a name="uploadMultipartForm"></a>
# **uploadMultipartForm**
> List uploadMultipartForm(file, contentType, filename, xFilename)

Upload an attachment for sending using Multipart Form

    When sending emails with attachments first upload each attachment with this endpoint. Record the returned attachment IDs. Then use these attachment IDs in the SendEmailOptions when sending an email. This means that attachments can easily be reused.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **File**| file | [default to null]
 **contentType** | **String**| contentType | [optional] [default to null]
 **filename** | **String**| filename | [optional] [default to null]
 **xFilename** | **String**| x-filename | [optional] [default to null]

### Return type

[**List**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

