# AliasControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAlias**](AliasControllerApi#createAlias) | **POST** /aliases | Create an email alias. Must be verified by clicking link inside verification email that will be sent to the address. Once verified the alias will be active.
[**deleteAlias**](AliasControllerApi#deleteAlias) | **DELETE** /aliases/{aliasId} | Delete an email alias
[**getAlias**](AliasControllerApi#getAlias) | **GET** /aliases/{aliasId} | Get an email alias
[**getAliasEmails**](AliasControllerApi#getAliasEmails) | **GET** /aliases/{aliasId}/emails | Get emails for an alias
[**getAliasThreads**](AliasControllerApi#getAliasThreads) | **GET** /aliases/{aliasId}/threads | Get threads created for an alias
[**getAliases**](AliasControllerApi#getAliases) | **GET** /aliases | Get all email aliases you have created
[**replyToAliasEmail**](AliasControllerApi#replyToAliasEmail) | **PUT** /aliases/{aliasId}/emails/{emailId} | Reply to an email
[**sendAliasEmail**](AliasControllerApi#sendAliasEmail) | **POST** /aliases/{aliasId}/emails | Send an email from an alias inbox
[**updateAlias**](AliasControllerApi#updateAlias) | **PUT** /aliases/{aliasId} | Update an email alias


<a name="createAlias"></a>
# **createAlias**
> AliasDto createAlias(createAliasOptions)

Create an email alias. Must be verified by clicking link inside verification email that will be sent to the address. Once verified the alias will be active.

    Email aliases use a MailSlurp randomly generated email address (or a custom domain inbox that you provide) to mask or proxy a real email address. Emails sent to the alias address will be forwarded to the hidden email address it was created for. If you want to send a reply use the threadId attached

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAliasOptions** | [**CreateAliasOptions**](../Models/CreateAliasOptions)| createAliasOptions |

### Return type

[**AliasDto**](../Models/AliasDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteAlias"></a>
# **deleteAlias**
> deleteAlias(aliasId)

Delete an email alias

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| aliasId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAlias"></a>
# **getAlias**
> AliasDto getAlias(aliasId)

Get an email alias

    Get an email alias by ID

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| aliasId | [default to null]

### Return type

[**AliasDto**](../Models/AliasDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAliasEmails"></a>
# **getAliasEmails**
> PageEmailProjection getAliasEmails(aliasId, before, page, since, size, sort)

Get emails for an alias

    Get paginated emails for an alias by ID

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| aliasId | [default to null]
 **before** | **Date**| Optional filter by sent before given date time | [optional] [default to null]
 **page** | **Integer**| Optional page index alias email list pagination | [optional] [default to 0]
 **since** | **Date**| Optional filter by sent after given date time | [optional] [default to null]
 **size** | **Integer**| Optional page size alias email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageEmailProjection**](../Models/PageEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAliasThreads"></a>
# **getAliasThreads**
> PageThreadProjection getAliasThreads(aliasId, before, page, since, size, sort)

Get threads created for an alias

    Returns threads created for an email alias in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| aliasId | [default to null]
 **before** | **Date**| Optional filter by sent before given date time | [optional] [default to null]
 **page** | **Integer**| Optional page index in thread list pagination | [optional] [default to 0]
 **since** | **Date**| Optional filter by sent after given date time | [optional] [default to null]
 **size** | **Integer**| Optional page size in thread list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageThreadProjection**](../Models/PageThreadProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getAliases"></a>
# **getAliases**
> PageAlias getAliases(before, page, since, size, sort)

Get all email aliases you have created

    Get all email aliases in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **page** | **Integer**| Optional page index in alias list pagination | [optional] [default to 0]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **size** | **Integer**| Optional page size in alias list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageAlias**](../Models/PageAlias)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="replyToAliasEmail"></a>
# **replyToAliasEmail**
> SentEmailDto replyToAliasEmail(aliasId, emailId, replyToAliasEmailOptions)

Reply to an email

    Send the reply to the email sender or reply-to and include same subject cc bcc etc. Reply to an email and the contents will be sent with the existing subject to the emails &#x60;to&#x60;, &#x60;cc&#x60;, and &#x60;bcc&#x60;.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| ID of the alias that email belongs to | [default to null]
 **emailId** | [**UUID**](../Models/)| ID of the email that should be replied to | [default to null]
 **replyToAliasEmailOptions** | [**ReplyToAliasEmailOptions**](../Models/ReplyToAliasEmailOptions)| replyToAliasEmailOptions |

### Return type

[**SentEmailDto**](../Models/SentEmailDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="sendAliasEmail"></a>
# **sendAliasEmail**
> SentEmailDto sendAliasEmail(aliasId, sendEmailOptions)

Send an email from an alias inbox

    Send an email from an alias. Replies to the email will be forwarded to the alias masked email address

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| aliasId | [default to null]
 **sendEmailOptions** | [**SendEmailOptions**](../Models/SendEmailOptions)| Options for the email to be sent | [optional]

### Return type

[**SentEmailDto**](../Models/SentEmailDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="updateAlias"></a>
# **updateAlias**
> updateAlias(aliasId, updateAliasOptions)

Update an email alias

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aliasId** | [**UUID**](../Models/)| aliasId | [default to null]
 **updateAliasOptions** | [**UpdateAliasOptions**](../Models/UpdateAliasOptions)| updateAliasOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

