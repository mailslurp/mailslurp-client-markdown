# CommonActionsControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewEmailAddress**](CommonActionsControllerApi#createNewEmailAddress) | **POST** /newEmailAddress | Create new random inbox
[**createRandomInbox**](CommonActionsControllerApi#createRandomInbox) | **POST** /createInbox | Create new random inbox
[**deleteEmailAddress**](CommonActionsControllerApi#deleteEmailAddress) | **DELETE** /deleteEmailAddress | Delete inbox email address by inbox id
[**emptyInbox**](CommonActionsControllerApi#emptyInbox) | **DELETE** /emptyInbox | Delete all emails in an inbox
[**sendEmailSimple**](CommonActionsControllerApi#sendEmailSimple) | **POST** /sendEmail | Send an email


<a name="createNewEmailAddress"></a>
# **createNewEmailAddress**
> InboxDto createNewEmailAddress(allowTeamAccess, useDomainPool, expiresAt, expiresIn, emailAddress, inboxType, description, name, tags, favourite)

Create new random inbox

    Returns an Inbox with an &#x60;id&#x60; and an &#x60;emailAddress&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowTeamAccess** | **Boolean**|  | [optional] [default to null]
 **useDomainPool** | **Boolean**|  | [optional] [default to null]
 **expiresAt** | **Date**|  | [optional] [default to null]
 **expiresIn** | **Long**|  | [optional] [default to null]
 **emailAddress** | **String**|  | [optional] [default to null]
 **inboxType** | **String**|  | [optional] [default to null] [enum: HTTP_INBOX, SMTP_INBOX]
 **description** | **String**|  | [optional] [default to null]
 **name** | **String**|  | [optional] [default to null]
 **tags** | [**List**](../Models/String)|  | [optional] [default to null]
 **favourite** | **Boolean**|  | [optional] [default to null]

### Return type

[**InboxDto**](../Models/InboxDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="createRandomInbox"></a>
# **createRandomInbox**
> InboxDto createRandomInbox(allowTeamAccess, useDomainPool, expiresAt, expiresIn, emailAddress, inboxType, description, name, tags, favourite)

Create new random inbox

    Returns an Inbox with an &#x60;id&#x60; and an &#x60;emailAddress&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowTeamAccess** | **Boolean**|  | [optional] [default to null]
 **useDomainPool** | **Boolean**|  | [optional] [default to null]
 **expiresAt** | **Date**|  | [optional] [default to null]
 **expiresIn** | **Long**|  | [optional] [default to null]
 **emailAddress** | **String**|  | [optional] [default to null]
 **inboxType** | **String**|  | [optional] [default to null] [enum: HTTP_INBOX, SMTP_INBOX]
 **description** | **String**|  | [optional] [default to null]
 **name** | **String**|  | [optional] [default to null]
 **tags** | [**List**](../Models/String)|  | [optional] [default to null]
 **favourite** | **Boolean**|  | [optional] [default to null]

### Return type

[**InboxDto**](../Models/InboxDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="deleteEmailAddress"></a>
# **deleteEmailAddress**
> deleteEmailAddress(inboxId)

Delete inbox email address by inbox id

    Deletes inbox email address

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="emptyInbox"></a>
# **emptyInbox**
> emptyInbox(inboxId)

Delete all emails in an inbox

    Deletes all emails

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="sendEmailSimple"></a>
# **sendEmailSimple**
> sendEmailSimple(SimpleSendEmailOptions)

Send an email

    If no senderId or inboxId provided a random email address will be used to send from.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SimpleSendEmailOptions** | [**SimpleSendEmailOptions**](../Models/SimpleSendEmailOptions)|  |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

