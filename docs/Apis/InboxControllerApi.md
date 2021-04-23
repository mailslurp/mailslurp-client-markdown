# InboxControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createInbox**](InboxControllerApi#createInbox) | **POST** /inboxes | Create an Inbox (email address)
[**createInboxWithOptions**](InboxControllerApi#createInboxWithOptions) | **POST** /inboxes/withOptions | Create an inbox with additional options
[**deleteAllInboxes**](InboxControllerApi#deleteAllInboxes) | **DELETE** /inboxes | Delete all inboxes
[**deleteInbox**](InboxControllerApi#deleteInbox) | **DELETE** /inboxes/{inboxId} | Delete inbox
[**getAllInboxes**](InboxControllerApi#getAllInboxes) | **GET** /inboxes/paginated | List All Inboxes Paginated
[**getEmails**](InboxControllerApi#getEmails) | **GET** /inboxes/{inboxId}/emails | Get emails in an Inbox. This method is not idempotent as it allows retries and waits if you want certain conditions to be met before returning. For simple listing and sorting of known emails use the email controller instead.
[**getInbox**](InboxControllerApi#getInbox) | **GET** /inboxes/{inboxId} | Get Inbox
[**getInboxEmailsPaginated**](InboxControllerApi#getInboxEmailsPaginated) | **GET** /inboxes/{inboxId}/emails/paginated | Get inbox emails paginated
[**getInboxSentEmails**](InboxControllerApi#getInboxSentEmails) | **GET** /inboxes/{inboxId}/sent | Get Inbox Sent Emails
[**getInboxTags**](InboxControllerApi#getInboxTags) | **GET** /inboxes/tags | Get inbox tags
[**getInboxes**](InboxControllerApi#getInboxes) | **GET** /inboxes | List Inboxes / Email Addresses
[**getOrganizationInboxes**](InboxControllerApi#getOrganizationInboxes) | **GET** /inboxes/organization | List Organization Inboxes Paginated
[**sendEmail**](InboxControllerApi#sendEmail) | **POST** /inboxes/{inboxId} | Send Email
[**sendEmailAndConfirm**](InboxControllerApi#sendEmailAndConfirm) | **POST** /inboxes/{inboxId}/confirm | Send email and return sent confirmation
[**setInboxFavourited**](InboxControllerApi#setInboxFavourited) | **PUT** /inboxes/{inboxId}/favourite | Set inbox favourited state
[**updateInbox**](InboxControllerApi#updateInbox) | **PATCH** /inboxes/{inboxId} | Update Inbox


<a name="createInbox"></a>
# **createInbox**
> Inbox createInbox(allowTeamAccess, description, emailAddress, expiresAt, expiresIn, favourite, name, tags, useDomainPool)

Create an Inbox (email address)

    Create a new inbox and with a randomized email address to send and receive from. Pass emailAddress parameter if you wish to use a specific email address. Creating an inbox is required before sending or receiving emails. If writing tests it is recommended that you create a new inbox during each test method so that it is unique and empty. 

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowTeamAccess** | **Boolean**| Grant team access to this inbox and the emails that belong to it for team members of your organization. | [optional] [default to null]
 **description** | **String**| Optional description of the inbox for labelling purposes. Is shown in the dashboard and can be used with | [optional] [default to null]
 **emailAddress** | **String**| A custom email address to use with the inbox. Defaults to null. When null MailSlurp will assign a random email address to the inbox such as &#x60;123@mailslurp.com&#x60;. If you use the &#x60;useDomainPool&#x60; option when the email address is null it will generate an email address with a more varied domain ending such as &#x60;123@mailslurp.info&#x60; or &#x60;123@mailslurp.biz&#x60;. When a custom email address is provided the address is split into a domain and the domain is queried against your user. If you have created the domain in the MailSlurp dashboard and verified it you can use any email address that ends with the domain. Send an email to this address and the inbox will receive and store it for you. To retrieve the email use the Inbox and Email Controller endpoints with the inbox ID. | [optional] [default to null]
 **expiresAt** | **Date**| Optional inbox expiration date. If null then this inbox is permanent and the emails in it won&#39;t be deleted. If an expiration date is provided or is required by your plan the inbox will be closed when the expiration time is reached. Expired inboxes still contain their emails but can no longer send or receive emails. An ExpiredInboxRecord is created when an inbox and the email address and inbox ID are recorded. The expiresAt property is a timestamp string in ISO DateTime Format yyyy-MM-dd&#39;T&#39;HH:mm:ss.SSSXXX. | [optional] [default to null]
 **expiresIn** | **Long**| Number of milliseconds that inbox should exist for | [optional] [default to null]
 **favourite** | **Boolean**| Is the inbox favorited. Favouriting inboxes is typically done in the dashboard for quick access or filtering | [optional] [default to null]
 **name** | **String**| Optional name of the inbox. Displayed in the dashboard for easier search | [optional] [default to null]
 **tags** | [**List**](..//Models/String)| Tags that inbox has been tagged with. Tags can be added to inboxes to group different inboxes within an account. You can also search for inboxes by tag in the dashboard UI. | [optional] [default to null]
 **useDomainPool** | **Boolean**| Use the MailSlurp domain name pool with this inbox when creating the email address. Defaults to null. If enabled the inbox will be an email address with a domain randomly chosen from a list of the MailSlurp domains. This is useful when the default &#x60;@mailslurp.com&#x60; email addresses used with inboxes are blocked or considered spam by a provider or receiving service. When domain pool is enabled an email address will be generated ending in &#x60;@mailslurp.{world,info,xyz,...}&#x60; . This means a TLD is randomly selecting from a list of &#x60;.biz&#x60;, &#x60;.info&#x60;, &#x60;.xyz&#x60; etc to add variance to the generated email addresses. When null or false MailSlurp uses the default behavior of &#x60;@mailslurp.com&#x60; or custom email address provided by the emailAddress field. | [optional] [default to null]

### Return type

[**Inbox**](..//Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="createInboxWithOptions"></a>
# **createInboxWithOptions**
> Inbox createInboxWithOptions(createInboxDto)

Create an inbox with additional options

    Additional endpoint that allows inbox creation with request body options. Can be more flexible that other methods for some clients.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createInboxDto** | [**CreateInboxDto**](..//Models/CreateInboxDto)| createInboxDto |

### Return type

[**Inbox**](..//Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
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

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteInbox"></a>
# **deleteInbox**
> deleteInbox(inboxId)

Delete inbox

    Permanently delete an inbox and associated email address as well as all emails within the given inbox. This action cannot be undone. Note: deleting an inbox will not affect your account usage. Monthly inbox usage is based on how many inboxes you create within 30 days, not how many exist at time of request.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllInboxes"></a>
# **getAllInboxes**
> PageInboxProjection getAllInboxes(favourite, page, search, size, sort, tag, teamAccess)

List All Inboxes Paginated

    List inboxes in paginated form. The results are available on the &#x60;content&#x60; property of the returned object. This method allows for page index (zero based), page size (how many results to return), and a sort direction (based on createdAt time). You Can also filter by whether an inbox is favorited or use email address pattern. This method is the recommended way to query inboxes. The alternative &#x60;getInboxes&#x60; method returns a full list of inboxes but is limited to 100 results. Results do not include team access inboxes by default. Use organization method to list team inboxes or set &#x60;teamAccess&#x60; to true.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **favourite** | **Boolean**| Optionally filter results for favourites only | [optional] [default to false]
 **page** | **Integer**| Optional page index in inbox list pagination | [optional] [default to 0]
 **search** | **String**| Optionally filter by search words partial matching ID, tags, name, and email address | [optional] [default to null]
 **size** | **Integer**| Optional page size in inbox list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **tag** | **String**| Optionally filter by tags. Will return inboxes that include given tags | [optional] [default to null]
 **teamAccess** | **Boolean**| Optionally filter by team access. Defaults to false so organization inboxes are not included | [optional] [default to false]

### Return type

[**PageInboxProjection**](..//Models/PageInboxProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEmails"></a>
# **getEmails**
> List getEmails(inboxId, limit, minCount, retryTimeout, since, size, sort)

Get emails in an Inbox. This method is not idempotent as it allows retries and waits if you want certain conditions to be met before returning. For simple listing and sorting of known emails use the email controller instead.

    List emails that an inbox has received. Only emails that are sent to the inbox&#39;s email address will appear in the inbox. It may take several seconds for any email you send to an inbox&#39;s email address to appear in the inbox. To make this endpoint wait for a minimum number of emails use the &#x60;minCount&#x60; parameter. The server will retry the inbox database until the &#x60;minCount&#x60; is satisfied or the &#x60;retryTimeout&#x60; is reached

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| Id of inbox that emails belongs to | [default to null]
 **limit** | **Integer**| Limit the result set, ordered by received date time sort direction. Maximum 100. For more listing options see the email controller | [optional] [default to null]
 **minCount** | **Long**| Minimum acceptable email count. Will cause request to hang (and retry) until minCount is satisfied or retryTimeout is reached. | [optional] [default to null]
 **retryTimeout** | **Long**| Maximum milliseconds to spend retrying inbox database until minCount emails are returned | [optional] [default to null]
 **since** | **Date**| Exclude emails received before this ISO 8601 date time | [optional] [default to null]
 **size** | **Integer**| Alias for limit. Assessed first before assessing any passed limit. | [optional] [default to null]
 **sort** | **String**| Sort the results by received date and direction ASC or DESC | [optional] [default to null] [enum: ASC, DESC]

### Return type

[**List**](..//Models/EmailPreview)

### Authorization

[API_KEY](../README#API_KEY)

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
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]

### Return type

[**Inbox**](..//Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxEmailsPaginated"></a>
# **getInboxEmailsPaginated**
> PageEmailPreview getInboxEmailsPaginated(inboxId, page, size, sort)

Get inbox emails paginated

    Get a paginated list of emails in an inbox. Does not hold connections open.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| Id of inbox that emails belongs to | [default to null]
 **page** | **Integer**| Optional page index in inbox emails list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox emails list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageEmailPreview**](..//Models/PageEmailPreview)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxSentEmails"></a>
# **getInboxSentEmails**
> PageSentEmailProjection getInboxSentEmails(inboxId, page, size, sort)

Get Inbox Sent Emails

    Returns an inbox&#39;s sent email receipts. Call individual sent email endpoints for more details. Note for privacy reasons the full body of sent emails is never stored. An MD5 hash hex is available for comparison instead.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]
 **page** | **Integer**| Optional page index in inbox sent email list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageSentEmailProjection**](..//Models/PageSentEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

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

[**List**](..//Models/string)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxes"></a>
# **getInboxes**
> List getInboxes(size, sort)

List Inboxes / Email Addresses

    List the inboxes you have created. Note use of the more advanced &#x60;getAllEmails&#x60; is recommended. You can provide a limit and sort parameter.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | **Integer**| Optional result size limit. Note an automatic limit of 100 results is applied. See the paginated &#x60;getAllEmails&#x60; for larger queries. | [optional] [default to 100]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**List**](..//Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getOrganizationInboxes"></a>
# **getOrganizationInboxes**
> PageOrganizationInboxProjection getOrganizationInboxes(page, size, sort)

List Organization Inboxes Paginated

    List organization inboxes in paginated form. These are inboxes created with &#x60;allowTeamAccess&#x60; flag enabled. Organization inboxes are &#x60;readOnly&#x60; for non-admin users. The results are available on the &#x60;content&#x60; property of the returned object. This method allows for page index (zero based), page size (how many results to return), and a sort direction (based on createdAt time). 

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in inbox list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageOrganizationInboxProjection**](..//Models/PageOrganizationInboxProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="sendEmail"></a>
# **sendEmail**
> sendEmail(inboxId, sendEmailOptions)

Send Email

    Send an email from an inbox&#39;s email address.  The request body should contain the &#x60;SendEmailOptions&#x60; that include recipients, attachments, body etc. See &#x60;SendEmailOptions&#x60; for all available properties. Note the &#x60;inboxId&#x60; refers to the inbox&#39;s id not the inbox&#39;s email address. See https://www.mailslurp.com/guides/ for more information on how to send emails. This method does not return a sent email entity due to legacy reasons. To send and get a sent email as returned response use the sister method &#x60;sendEmailAndConfirm&#x60;.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| ID of the inbox you want to send the email from | [default to null]
 **sendEmailOptions** | [**SendEmailOptions**](..//Models/SendEmailOptions)| Options for the email | [optional]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

<a name="sendEmailAndConfirm"></a>
# **sendEmailAndConfirm**
> SentEmailDto sendEmailAndConfirm(inboxId, sendEmailOptions)

Send email and return sent confirmation

    Sister method for standard &#x60;sendEmail&#x60; method with the benefit of returning a &#x60;SentEmail&#x60; entity confirming the successful sending of the email with link the the sent object created for it.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| ID of the inbox you want to send the email from | [default to null]
 **sendEmailOptions** | [**SendEmailOptions**](..//Models/SendEmailOptions)| Options for the email | [optional]

### Return type

[**SentEmailDto**](..//Models/SentEmailDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="setInboxFavourited"></a>
# **setInboxFavourited**
> Inbox setInboxFavourited(inboxId, setInboxFavouritedOptions)

Set inbox favourited state

    Set and return new favourite state for an inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]
 **setInboxFavouritedOptions** | [**SetInboxFavouritedOptions**](..//Models/SetInboxFavouritedOptions)| setInboxFavouritedOptions |

### Return type

[**Inbox**](..//Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

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
 **inboxId** | [**UUID**](..//Models/)| inboxId | [default to null]
 **updateInboxOptions** | [**UpdateInboxOptions**](..//Models/UpdateInboxOptions)| updateInboxOptions |

### Return type

[**Inbox**](..//Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

