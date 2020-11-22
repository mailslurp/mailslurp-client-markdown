# EmailControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteAllEmails**](EmailControllerApi.md#deleteAllEmails) | **DELETE** /emails | Delete all emails
[**deleteEmail**](EmailControllerApi.md#deleteEmail) | **DELETE** /emails/{emailId} | Delete an email
[**downloadAttachment**](EmailControllerApi.md#downloadAttachment) | **GET** /emails/{emailId}/attachments/{attachmentId} | Get email attachment bytes. If you have trouble with byte responses try the &#x60;downloadAttachmentBase64&#x60; response endpoints.
[**downloadAttachmentBase64**](EmailControllerApi.md#downloadAttachmentBase64) | **GET** /emails/{emailId}/attachments/{attachmentId}/base64 | Get email attachment as base64 encoded string (alternative to binary responses)
[**forwardEmail**](EmailControllerApi.md#forwardEmail) | **POST** /emails/{emailId}/forward | Forward email
[**getAttachmentMetaData**](EmailControllerApi.md#getAttachmentMetaData) | **GET** /emails/{emailId}/attachments/{attachmentId}/metadata | Get email attachment metadata
[**getAttachments**](EmailControllerApi.md#getAttachments) | **GET** /emails/{emailId}/attachments | Get all email attachment metadata
[**getEmail**](EmailControllerApi.md#getEmail) | **GET** /emails/{emailId} | Get email content
[**getEmailContentMatch**](EmailControllerApi.md#getEmailContentMatch) | **GET** /emails/{emailId}/contentMatch | Get email content regex pattern match results. Runs regex against email body and returns match groups.
[**getEmailHTML**](EmailControllerApi.md#getEmailHTML) | **GET** /emails/{emailId}/html | Get email content as HTML
[**getEmailsPaginated**](EmailControllerApi.md#getEmailsPaginated) | **GET** /emails | Get all emails
[**getRawEmailContents**](EmailControllerApi.md#getRawEmailContents) | **GET** /emails/{emailId}/raw | Get raw email string
[**getRawEmailJson**](EmailControllerApi.md#getRawEmailJson) | **GET** /emails/{emailId}/raw/json | Get raw email in JSON
[**getUnreadEmailCount**](EmailControllerApi.md#getUnreadEmailCount) | **GET** /emails/unreadCount | Get unread email count
[**validateEmail**](EmailControllerApi.md#validateEmail) | **POST** /emails/{emailId}/validate | Validate email


<a name="deleteAllEmails"></a>
# **deleteAllEmails**
> deleteAllEmails()

Delete all emails

    Deletes all emails in your account. Be careful as emails cannot be recovered

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteEmail"></a>
# **deleteEmail**
> deleteEmail(emailId)

Delete an email

    Deletes an email and removes it from the inbox. Deleted emails cannot be recovered.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email to delete | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="downloadAttachment"></a>
# **downloadAttachment**
> byte[] downloadAttachment(attachmentId, emailId, apiKey)

Get email attachment bytes. If you have trouble with byte responses try the &#x60;downloadAttachmentBase64&#x60; response endpoints.

    Returns the specified attachment for a given email as a stream / array of bytes. You can find attachment ids in email responses endpoint responses. The response type is application/octet-stream.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]
 **apiKey** | **String**| Can pass apiKey in url for this request if you wish to download the file in a browser. Content type will be set to original content type of the attachment file. This is so that browsers can download the file correctly. | [optional] [default to null]

### Return type

[**byte[]**](..//Models/ByteArray.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream

<a name="downloadAttachmentBase64"></a>
# **downloadAttachmentBase64**
> DownloadAttachmentDto downloadAttachmentBase64(attachmentId, emailId)

Get email attachment as base64 encoded string (alternative to binary responses)

    Returns the specified attachment for a given email as a base 64 encoded string. The response type is application/json. This method is similar to the &#x60;downloadAttachment&#x60; method but allows some clients to get around issues with binary responses.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]

### Return type

[**DownloadAttachmentDto**](..//Models/DownloadAttachmentDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="forwardEmail"></a>
# **forwardEmail**
> forwardEmail(emailId, forwardEmailOptions)

Forward email

    Forward an existing email to new recipients.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]
 **forwardEmailOptions** | [**ForwardEmailOptions**](..//Models/ForwardEmailOptions.md)| forwardEmailOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

<a name="getAttachmentMetaData"></a>
# **getAttachmentMetaData**
> AttachmentMetaData getAttachmentMetaData(attachmentId, emailId)

Get email attachment metadata

    Returns the metadata such as name and content-type for a given attachment and email.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachmentId** | **String**| ID of attachment | [default to null]
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]

### Return type

[**AttachmentMetaData**](..//Models/AttachmentMetaData.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAttachments"></a>
# **getAttachments**
> List getAttachments(emailId)

Get all email attachment metadata

    Returns an array of attachment metadata such as name and content-type for a given email if present.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]

### Return type

[**List**](..//Models/AttachmentMetaData.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEmail"></a>
# **getEmail**
> Email getEmail(emailId, decode)

Get email content

    Returns a email summary object with headers and content. To retrieve the raw unparsed email use the getRawEmail endpoints

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| emailId | [default to null]
 **decode** | **Boolean**| Decode email body quoted-printable encoding to plain text. SMTP servers often encode text using quoted-printable format (for instance &#x60;&#x3D;D7&#x60;). This can be a pain for testing | [optional] [default to false]

### Return type

[**Email**](..//Models/Email.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEmailContentMatch"></a>
# **getEmailContentMatch**
> EmailContentMatchResult getEmailContentMatch(emailId, contentMatchOptions)

Get email content regex pattern match results. Runs regex against email body and returns match groups.

    Return the matches for a given Java style regex pattern. Do not include the typical &#x60;/&#x60; at start or end of regex in some languages. Given an example &#x60;your code is: 12345&#x60; the pattern to extract match looks like &#x60;code is: (\\d{6})&#x60;. This will return an array of matches with the first matching the entire pattern and the subsequent matching the groups: &#x60;[&#39;code is: 123456&#39;, &#39;123456&#39;]&#x60; See https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html for more information of available patterns.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email to match against | [default to null]
 **contentMatchOptions** | [**ContentMatchOptions**](..//Models/ContentMatchOptions.md)| contentMatchOptions |

### Return type

[**EmailContentMatchResult**](..//Models/EmailContentMatchResult.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="getEmailHTML"></a>
# **getEmailHTML**
> String getEmailHTML(emailId, decode)

Get email content as HTML

    Retrieve email content as HTML response for viewing in browsers. Decodes quoted-printable entities and converts charset to UTF-8. Pass your API KEY as a request parameter when viewing in a browser: &#x60;?apiKey&#x3D;xxx&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| emailId | [default to null]
 **decode** | **Boolean**| decode | [optional] [default to false]

### Return type

[**String**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/html

<a name="getEmailsPaginated"></a>
# **getEmailsPaginated**
> PageEmailProjection getEmailsPaginated(inboxId, page, size, sort, unreadOnly)

Get all emails

    By default returns all emails across all inboxes sorted by ascending created at date. Responses are paginated. You can restrict results to a list of inbox IDs. You can also filter out read messages

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**List**](..//Models/UUID.md)| Optional inbox ids to filter by. Can be repeated. By default will use all inboxes belonging to your account. | [optional] [default to null]
 **page** | **Integer**| Optional page index in email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **unreadOnly** | **Boolean**| Optional filter for unread emails only. All emails are considered unread until they are viewed in the dashboard or requested directly | [optional] [default to false]

### Return type

[**PageEmailProjection**](..//Models/PageEmailProjection.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getRawEmailContents"></a>
# **getRawEmailContents**
> String getRawEmailContents(emailId)

Get raw email string

    Returns a raw, unparsed, and unprocessed email. If your client has issues processing the response it is likely due to the response content-type which is text/plain. If you need a JSON response content-type use the getRawEmailJson endpoint

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]

### Return type

[**String**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain

<a name="getRawEmailJson"></a>
# **getRawEmailJson**
> RawEmailJson getRawEmailJson(emailId)

Get raw email in JSON

    Returns a raw, unparsed, and unprocessed email wrapped in a JSON response object for easier handling when compared with the getRawEmail text/plain response

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]

### Return type

[**RawEmailJson**](..//Models/RawEmailJson.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getUnreadEmailCount"></a>
# **getUnreadEmailCount**
> UnreadCount getUnreadEmailCount()

Get unread email count

    Get number of emails unread

### Parameters
This endpoint does not need any parameter.

### Return type

[**UnreadCount**](..//Models/UnreadCount.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="validateEmail"></a>
# **validateEmail**
> ValidationDto validateEmail(emailId)

Validate email

    Validate the HTML content of email if HTML is found. Considered valid if no HTML.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/.md)| ID of email | [default to null]

### Return type

[**ValidationDto**](..//Models/ValidationDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

