# InboxControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createInbox**](InboxControllerApi.md#createInbox) | **POST** /inboxes | Create an Inbox (email address)
[**deleteAllInboxes**](InboxControllerApi.md#deleteAllInboxes) | **DELETE** /inboxes | Delete all inboxes
[**deleteInbox**](InboxControllerApi.md#deleteInbox) | **DELETE** /inboxes/{inboxId} | Delete inbox
[**getAllInboxes**](InboxControllerApi.md#getAllInboxes) | **GET** /inboxes/paginated | List Inboxes Paginated
[**getEmails**](InboxControllerApi.md#getEmails) | **GET** /inboxes/{inboxId}/emails | Get emails in an Inbox
[**getInbox**](InboxControllerApi.md#getInbox) | **GET** /inboxes/{inboxId} | Get Inbox
[**getInboxEmailsPaginated**](InboxControllerApi.md#getInboxEmailsPaginated) | **GET** /inboxes/{inboxId}/emails/paginated | Get inbox emails paginated
[**getInboxSentEmails**](InboxControllerApi.md#getInboxSentEmails) | **GET** /inboxes/{inboxId}/sent | Get Inbox Sent Emails
[**getInboxTags**](InboxControllerApi.md#getInboxTags) | **GET** /inboxes/tags | Get inbox tags
[**getInboxes**](InboxControllerApi.md#getInboxes) | **GET** /inboxes | List Inboxes / Email Addresses
[**sendEmail**](InboxControllerApi.md#sendEmail) | **POST** /inboxes/{inboxId} | Send Email
[**setInboxFavourited**](InboxControllerApi.md#setInboxFavourited) | **PUT** /inboxes/{inboxId}/favourite | Set inbox favourited state
[**updateInbox**](InboxControllerApi.md#updateInbox) | **PATCH** /inboxes/{inboxId} | Update Inbox


<a name="createInbox"></a>
# **createInbox**
> Inbox createInbox(description, emailAddress, expiresAt, favourite, name, tags)

Create an Inbox (email address)

    Create a new inbox and with a randomized email address to send and receive from. Pass emailAddress parameter if you wish to use a specific email address. Creating an inbox is required before sending or receiving emails. If writing tests it is recommended that you create a new inbox during each test method so that it is unique and empty. 

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **description** | **String**| Optional description for an inbox. | [optional] [default to null]
 **emailAddress** | **String**| Optional email address including domain you wish inbox to use (eg: test123@mydomain.com). Only supports domains that you have registered and verified with MailSlurp using dashboard or &#x60;createDomain&#x60; method. | [optional] [default to null]
 **expiresAt** | **Date**| Optional expires at timestamp. If your plan supports this feature you can specify when an inbox should expire. If left empty inbox will exist permanently or expire when your plan dictates | [optional] [default to null]
 **favourite** | **Boolean**| Is inbox favourited. | [optional] [default to null]
 **name** | **String**| Optional name for an inbox. | [optional] [default to null]
 **tags** | [**List**](..//Models/String.md)| Optional tags for an inbox. Can be used for searching and filtering inboxes. | [optional] [default to null]

### Return type

[**Inbox**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="deleteAllInboxes"></a>
# **deleteAllInboxes**
> deleteAllInboxes()

Delete all inboxes

    Permanently delete all inboxes and associated email addresses. This will also delete all emails within the inboxes. Be careful as inboxes cannot be recovered once deleted. Note: deleting inboxes will not impact your usage limits. Monthly inbox creation limits are based on how many inboxes were created in the last 30 days, not how many inboxes you currently have.

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteInbox"></a>
# **deleteInbox**
> deleteInbox(inboxId)

Delete inbox

    Permanently delete an inbox and associated email address aswell as all emails within the given inbox. This action cannot be undone. Note: deleting an inbox will not affect your account usage. Monthly inbox usage is based on how many inboxes you create within 30 days, not how many exist at time of request.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| inboxId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllInboxes"></a>
# **getAllInboxes**
> Page_InboxProjection_ getAllInboxes(favourite, page, search, size, sort, tag)

List Inboxes Paginated

    List inboxes in paginated form. Allows for page index, page size, and sort direction. Can also filter by favourited or email address like pattern.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **favourite** | **Boolean**| Optionally filter results for favourites only | [optional] [default to false]
 **page** | **Integer**| Optional page index in inbox list pagination | [optional] [default to 0]
 **search** | **String**| Optionally filter by search words partial matching ID, tags, name, and email address | [optional] [default to null]
 **size** | **Integer**| Optional page size in inbox list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **tag** | **String**| Optionally filter by tags | [optional] [default to null]

### Return type

[**Page_InboxProjection_**](..//Models/Page_InboxProjection_.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEmails"></a>
# **getEmails**
> List getEmails(inboxId, limit, minCount, retryTimeout, since, sort)

Get emails in an Inbox

    List emails that an inbox has received. Only emails that are sent to the inbox&#39;s email address will appear in the inbox. It may take several seconds for any email you send to an inbox&#39;s email address to appear in the inbox. To make this endpoint wait for a minimum number of emails use the &#x60;minCount&#x60; parameter. The server will retry the inbox database until the &#x60;minCount&#x60; is satisfied or the &#x60;retryTimeout&#x60; is reached

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| Id of inbox that emails belongs to | [default to null]
 **limit** | **Integer**| Limit the result set, ordered by received date time sort direction | [optional] [default to null]
 **minCount** | **Long**| Minimum acceptable email count. Will cause request to hang (and retry) until minCount is satisfied or retryTimeout is reached. | [optional] [default to null]
 **retryTimeout** | **Long**| Maximum milliseconds to spend retrying inbox database until minCount emails are returned | [optional] [default to null]
 **since** | **Date**| Exclude emails received before this ISO 8601 date time | [optional] [default to null]
 **sort** | **String**| Sort the results by received date and direction ASC or DESC | [optional] [default to null] [enum: ASC, DESC]

### Return type

[**List**](..//Models/EmailPreview.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInbox"></a>
# **getInbox**
> Inbox getInbox(inboxId)

Get Inbox

    Returns an inbox&#39;s properties, including its email address and ID.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| inboxId | [default to null]

### Return type

[**Inbox**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxEmailsPaginated"></a>
# **getInboxEmailsPaginated**
> Page_EmailPreview_ getInboxEmailsPaginated(inboxId, page, size, sort)

Get inbox emails paginated

    Get a paginated list of emails in an inbox. Does not hold connections open.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| Id of inbox that emails belongs to | [default to null]
 **page** | **Integer**| Optional page index in inbox emails list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox emails list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**Page_EmailPreview_**](..//Models/Page_EmailPreview_.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxSentEmails"></a>
# **getInboxSentEmails**
> Page_SentEmailProjection_ getInboxSentEmails(inboxId, page, size, sort)

Get Inbox Sent Emails

    Returns an inbox&#39;s sent email receipts. Call individual sent email endpoints for more details. Note for privacy reasons the full body of sent emails is never stored. An MD5 hash hex is available for comparison instead.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| inboxId | [default to null]
 **page** | **Integer**| Optional page index in inbox sent email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**Page_SentEmailProjection_**](..//Models/Page_SentEmailProjection_.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxTags"></a>
# **getInboxTags**
> List getInboxTags()

Get inbox tags

    Get all inbox tags

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](..//Models/string.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxes"></a>
# **getInboxes**
> List getInboxes()

List Inboxes / Email Addresses

    List the inboxes you have created

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="sendEmail"></a>
# **sendEmail**
> sendEmail(inboxId, sendEmailOptions)

Send Email

    Send an email from an inbox&#39;s email address.  The request body should contain the &#x60;SendEmailOptions&#x60; that include recipients, attachments, body etc. See &#x60;SendEmailOptions&#x60; for all available properties. Note the &#x60;inboxId&#x60; refers to the inbox&#39;s id not the inbox&#39;s email address. See https://www.mailslurp.com/guides/ for more information on how to send emails.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| ID of the inbox you want to send the email from | [default to null]
 **sendEmailOptions** | [**SendEmailOptions**](..//Models/SendEmailOptions.md)| Options for the email | [optional]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

<a name="setInboxFavourited"></a>
# **setInboxFavourited**
> Inbox setInboxFavourited(inboxId, setInboxFavouritedOptions)

Set inbox favourited state

    Set and return new favourite state for an inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| inboxId | [default to null]
 **setInboxFavouritedOptions** | [**SetInboxFavouritedOptions**](..//Models/SetInboxFavouritedOptions.md)| setInboxFavouritedOptions |

### Return type

[**Inbox**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="updateInbox"></a>
# **updateInbox**
> Inbox updateInbox(inboxId, updateInboxOptions)

Update Inbox

    Update editable fields on an inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/.md)| inboxId | [default to null]
 **updateInboxOptions** | [**UpdateInboxOptions**](..//Models/UpdateInboxOptions.md)| updateInboxOptions |

### Return type

[**Inbox**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

