# EmailControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteAllEmails**](EmailControllerApi#deleteAllEmails) | **DELETE** /emails | Delete all emails
[**deleteEmail**](EmailControllerApi#deleteEmail) | **DELETE** /emails/{emailId} | Delete an email
[**downloadAttachment**](EmailControllerApi#downloadAttachment) | **GET** /emails/{emailId}/attachments/{attachmentId} | Get email attachment bytes. If you have trouble with byte responses try the &#x60;downloadAttachmentBase64&#x60; response endpoints.
[**downloadAttachmentBase64**](EmailControllerApi#downloadAttachmentBase64) | **GET** /emails/{emailId}/attachments/{attachmentId}/base64 | Get email attachment as base64 encoded string (alternative to binary responses)
[**forwardEmail**](EmailControllerApi#forwardEmail) | **POST** /emails/{emailId}/forward | Forward email
[**getAttachmentMetaData**](EmailControllerApi#getAttachmentMetaData) | **GET** /emails/{emailId}/attachments/{attachmentId}/metadata | Get email attachment metadata
[**getAttachments**](EmailControllerApi#getAttachments) | **GET** /emails/{emailId}/attachments | Get all email attachment metadata
[**getEmail**](EmailControllerApi#getEmail) | **GET** /emails/{emailId} | Get email content
[**getEmailContentMatch**](EmailControllerApi#getEmailContentMatch) | **POST** /emails/{emailId}/contentMatch | Get email content regex pattern match results. Runs regex against email body and returns match groups.
[**getEmailHTML**](EmailControllerApi#getEmailHTML) | **GET** /emails/{emailId}/html | Get email content as HTML
[**getEmailHTMLQuery**](EmailControllerApi#getEmailHTMLQuery) | **GET** /emails/{emailId}/htmlQuery | Parse and return text from an email, stripping HTML and decoding encoded characters
[**getEmailTextLines**](EmailControllerApi#getEmailTextLines) | **GET** /emails/{emailId}/textLines | Parse and return text from an email, stripping HTML and decoding encoded characters
[**getEmailsPaginated**](EmailControllerApi#getEmailsPaginated) | **GET** /emails | Get all emails
[**getLatestEmail**](EmailControllerApi#getLatestEmail) | **GET** /emails/latest | Get latest email
[**getLatestEmailInInbox**](EmailControllerApi#getLatestEmailInInbox) | **GET** /emails/latestIn | Get latest email
[**getOrganizationEmailsPaginated**](EmailControllerApi#getOrganizationEmailsPaginated) | **GET** /emails/organization | Get all organization emails
[**getRawEmailContents**](EmailControllerApi#getRawEmailContents) | **GET** /emails/{emailId}/raw | Get raw email string
[**getRawEmailJson**](EmailControllerApi#getRawEmailJson) | **GET** /emails/{emailId}/raw/json | Get raw email in JSON
[**getUnreadEmailCount**](EmailControllerApi#getUnreadEmailCount) | **GET** /emails/unreadCount | Get unread email count
[**replyToEmail**](EmailControllerApi#replyToEmail) | **PUT** /emails/{emailId} | Reply to an email
[**validateEmail**](EmailControllerApi#validateEmail) | **POST** /emails/{emailId}/validate | Validate email


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

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email to delete | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]
 **apiKey** | **String**| Can pass apiKey in url for this request if you wish to download the file in a browser. Content type will be set to original content type of the attachment file. This is so that browsers can download the file correctly. | [optional] [default to null]

### Return type

[**byte[]**](..//Models/ByteArray)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]

### Return type

[**DownloadAttachmentDto**](..//Models/DownloadAttachmentDto)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]
 **forwardEmailOptions** | [**ForwardEmailOptions**](..//Models/ForwardEmailOptions)| forwardEmailOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]

### Return type

[**AttachmentMetaData**](..//Models/AttachmentMetaData)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]

### Return type

[**List**](..//Models/AttachmentMetaData)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| emailId | [default to null]
 **decode** | **Boolean**| Decode email body quoted-printable encoding to plain text. SMTP servers often encode text using quoted-printable format (for instance &#x60;&#x3D;D7&#x60;). This can be a pain for testing | [optional] [default to false]

### Return type

[**Email**](..//Models/Email)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email to match against | [default to null]
 **contentMatchOptions** | [**ContentMatchOptions**](..//Models/ContentMatchOptions)| contentMatchOptions |

### Return type

[**EmailContentMatchResult**](..//Models/EmailContentMatchResult)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| emailId | [default to null]
 **decode** | **Boolean**| decode | [optional] [default to false]

### Return type

[**String**](..//Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/html

<a name="getEmailHTMLQuery"></a>
# **getEmailHTMLQuery**
> EmailTextLinesResult getEmailHTMLQuery(emailId, htmlSelector)

Parse and return text from an email, stripping HTML and decoding encoded characters

    Parse an email body and return the content as an array of text. HTML parsing uses JSoup which supports JQuery/CSS style selectors

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/)| ID of email to perform HTML query on | [default to null]
 **htmlSelector** | **String**| HTML selector to search for. Uses JQuery/JSoup/CSS style selector like &#39;.my-div&#39; to match content. See https://jsoup.org/apidocs/org/jsoup/select/Selector.html for more information. | [optional] [default to null]

### Return type

[**EmailTextLinesResult**](..//Models/EmailTextLinesResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEmailTextLines"></a>
# **getEmailTextLines**
> EmailTextLinesResult getEmailTextLines(emailId, decodeHtmlEntities, lineSeparator)

Parse and return text from an email, stripping HTML and decoding encoded characters

    Parse an email body and return the content as an array of strings. HTML parsing uses JSoup and UNIX line separators.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/)| ID of email to fetch text for | [default to null]
 **decodeHtmlEntities** | **Boolean**| Decode HTML entities | [optional] [default to null]
 **lineSeparator** | **String**| Line separator character | [optional] [default to null]

### Return type

[**EmailTextLinesResult**](..//Models/EmailTextLinesResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEmailsPaginated"></a>
# **getEmailsPaginated**
> PageEmailProjection getEmailsPaginated(inboxId, page, size, sort, unreadOnly)

Get all emails

    By default returns all emails across all inboxes sorted by ascending created at date. Responses are paginated. You can restrict results to a list of inbox IDs. You can also filter out read messages

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**List**](..//Models/UUID)| Optional inbox ids to filter by. Can be repeated. By default will use all inboxes belonging to your account. | [optional] [default to null]
 **page** | **Integer**| Optional page index in email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in email list pagination. Maximum size is 100. Use page index and sort to page through larger results | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **unreadOnly** | **Boolean**| Optional filter for unread emails only. All emails are considered unread until they are viewed in the dashboard or requested directly | [optional] [default to false]

### Return type

[**PageEmailProjection**](..//Models/PageEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getLatestEmail"></a>
# **getLatestEmail**
> Email getLatestEmail(inboxIds)

Get latest email

    Get the newest email in all inboxes or in a passed set of inbox IDs

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxIds** | [**List**](..//Models/UUID)| Optional set of inboxes to filter by. Only get the latest email from these inbox IDs | [optional] [default to null]

### Return type

[**Email**](..//Models/Email)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getLatestEmailInInbox"></a>
# **getLatestEmailInInbox**
> Email getLatestEmailInInbox(inboxId)

Get latest email

    Get the newest email in all inboxes or in a passed set of inbox IDs

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| ID of the inbox you want to get the latest email from | [optional] [default to null]

### Return type

[**Email**](..//Models/Email)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getOrganizationEmailsPaginated"></a>
# **getOrganizationEmailsPaginated**
> PageEmailProjection getOrganizationEmailsPaginated(inboxId, page, size, sort, unreadOnly)

Get all organization emails

    By default returns all emails across all team inboxes sorted by ascending created at date. Responses are paginated. You can restrict results to a list of inbox IDs. You can also filter out read messages

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**List**](..//Models/UUID)| Optional inbox ids to filter by. Can be repeated. By default will use all inboxes belonging to your account. | [optional] [default to null]
 **page** | **Integer**| Optional page index in email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in email list pagination. Maximum size is 100. Use page index and sort to page through larger results | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **unreadOnly** | **Boolean**| Optional filter for unread emails only. All emails are considered unread until they are viewed in the dashboard or requested directly | [optional] [default to false]

### Return type

[**PageEmailProjection**](..//Models/PageEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]

### Return type

[**String**](..//Models/string)

### Authorization

[API_KEY](../README#API_KEY)

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
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]

### Return type

[**RawEmailJson**](..//Models/RawEmailJson)

### Authorization

[API_KEY](../README#API_KEY)

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

[**UnreadCount**](..//Models/UnreadCount)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="replyToEmail"></a>
# **replyToEmail**
> SentEmailDto replyToEmail(emailId, replyToEmailOptions)

Reply to an email

    Send the reply to the email sender or reply-to and include same subject cc bcc etc. Reply to an email and the contents will be sent with the existing subject to the emails &#x60;to&#x60;, &#x60;cc&#x60;, and &#x60;bcc&#x60;.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/)| ID of the email that should be replied to | [default to null]
 **replyToEmailOptions** | [**ReplyToEmailOptions**](..//Models/ReplyToEmailOptions)| replyToEmailOptions |

### Return type

[**SentEmailDto**](..//Models/SentEmailDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="validateEmail"></a>
# **validateEmail**
> ValidationDto validateEmail(emailId)

Validate email

    Validate the HTML content of email if HTML is found. Considered valid if no HTML.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailId** | [**UUID**](..//Models/)| ID of email | [default to null]

### Return type

[**ValidationDto**](..//Models/ValidationDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
