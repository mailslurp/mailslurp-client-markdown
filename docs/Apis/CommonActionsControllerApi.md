# CommonActionsControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewEmailAddress**](CommonActionsControllerApi#createNewEmailAddress) | **POST** /createInbox | Create new random inbox
[**createNewEmailAddress1**](CommonActionsControllerApi#createNewEmailAddress1) | **POST** /newEmailAddress | Create new random inbox
[**emptyInbox**](CommonActionsControllerApi#emptyInbox) | **DELETE** /emptyInbox | Delete all emails in an inbox
[**sendEmailSimple**](CommonActionsControllerApi#sendEmailSimple) | **POST** /sendEmail | Send an email


<a name="createNewEmailAddress"></a>
# **createNewEmailAddress**
> Inbox createNewEmailAddress(allowTeamAccess, description, emailAddress, expiresAt, expiresIn, favourite, inboxType, name, tags, useDomainPool)

Create new random inbox

    Returns an Inbox with an &#x60;id&#x60; and an &#x60;emailAddress&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowTeamAccess** | **Boolean**| allowTeamAccess | [optional] [default to null]
 **description** | **String**| description | [optional] [default to null]
 **emailAddress** | **String**| emailAddress | [optional] [default to null]
 **expiresAt** | **Date**| expiresAt | [optional] [default to null]
 **expiresIn** | **Long**| expiresIn | [optional] [default to null]
 **favourite** | **Boolean**| favourite | [optional] [default to null]
 **inboxType** | **String**| inboxType | [optional] [default to null] [enum: HTTP_INBOX, SMTP_INBOX]
 **name** | **String**| name | [optional] [default to null]
 **tags** | [**List**](../Models/String)| tags | [optional] [default to null]
 **useDomainPool** | **Boolean**| useDomainPool | [optional] [default to null]

### Return type

[**Inbox**](../Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="createNewEmailAddress1"></a>
# **createNewEmailAddress1**
> Inbox createNewEmailAddress1(allowTeamAccess, description, emailAddress, expiresAt, expiresIn, favourite, inboxType, name, tags, useDomainPool)

Create new random inbox

    Returns an Inbox with an &#x60;id&#x60; and an &#x60;emailAddress&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowTeamAccess** | **Boolean**| allowTeamAccess | [optional] [default to null]
 **description** | **String**| description | [optional] [default to null]
 **emailAddress** | **String**| emailAddress | [optional] [default to null]
 **expiresAt** | **Date**| expiresAt | [optional] [default to null]
 **expiresIn** | **Long**| expiresIn | [optional] [default to null]
 **favourite** | **Boolean**| favourite | [optional] [default to null]
 **inboxType** | **String**| inboxType | [optional] [default to null] [enum: HTTP_INBOX, SMTP_INBOX]
 **name** | **String**| name | [optional] [default to null]
 **tags** | [**List**](../Models/String)| tags | [optional] [default to null]
 **useDomainPool** | **Boolean**| useDomainPool | [optional] [default to null]

### Return type

[**Inbox**](../Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="emptyInbox"></a>
# **emptyInbox**
> emptyInbox(inboxId)

Delete all emails in an inbox

    Deletes all emails

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| inboxId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="sendEmailSimple"></a>
# **sendEmailSimple**
> sendEmailSimple(emailOptions)

Send an email

    If no senderId or inboxId provided a random email address will be used to send from.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailOptions** | [**SimpleSendEmailOptions**](../Models/SimpleSendEmailOptions)| emailOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

