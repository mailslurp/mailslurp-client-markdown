# CommonActionsControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewEmailAddress**](CommonActionsControllerApi.md#createNewEmailAddress) | **POST** /createInbox | Create new random inbox
[**createNewEmailAddress1**](CommonActionsControllerApi.md#createNewEmailAddress1) | **POST** /newEmailAddress | Create new random inbox
[**emptyInbox**](CommonActionsControllerApi.md#emptyInbox) | **DELETE** /emptyInbox | Delete all emails in an inbox
[**sendEmailSimple**](CommonActionsControllerApi.md#sendEmailSimple) | **POST** /sendEmail | Send an email


<a name="createNewEmailAddress"></a>
# **createNewEmailAddress**
> Inbox createNewEmailAddress(expiresAt, expiresIn, useDomainPool)

Create new random inbox

    Returns an Inbox with an &#x60;id&#x60; and an &#x60;emailAddress&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **expiresAt** | **Date**| expiresAt | [optional] [default to null]
 **expiresIn** | **Long**| expiresIn | [optional] [default to null]
 **useDomainPool** | **Boolean**| useDomainPool | [optional] [default to null]

### Return type

[**Inbox**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="createNewEmailAddress1"></a>
# **createNewEmailAddress1**
> Inbox createNewEmailAddress1(expiresAt, expiresIn, useDomainPool)

Create new random inbox

    Returns an Inbox with an &#x60;id&#x60; and an &#x60;emailAddress&#x60;

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **expiresAt** | **Date**| expiresAt | [optional] [default to null]
 **expiresIn** | **Long**| expiresIn | [optional] [default to null]
 **useDomainPool** | **Boolean**| useDomainPool | [optional] [default to null]

### Return type

[**Inbox**](..//Models/Inbox.md)

### Authorization

[API_KEY](../README.md#API_KEY)

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
 **inboxId** | [**UUID**](..//Models/.md)| inboxId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

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
 **emailOptions** | [**SimpleSendEmailOptions**](..//Models/SimpleSendEmailOptions.md)| emailOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

