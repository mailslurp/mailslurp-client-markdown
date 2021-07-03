# MissedEmailControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllMissedEmails**](MissedEmailControllerApi#getAllMissedEmails) | **GET** /missed-emails | Get all MissedEmails in paginated format
[**getMissedEmail**](MissedEmailControllerApi#getMissedEmail) | **GET** /missed-emails/{missedEmailId} | Get MissedEmail
[**waitForNthMissedEmail**](MissedEmailControllerApi#waitForNthMissedEmail) | **GET** /missed-emails/waitForNthMissedEmail | Wait for Nth missed email


<a name="getAllMissedEmails"></a>
# **getAllMissedEmails**
> PageMissedEmailProjection getAllMissedEmails(inboxId, page, searchFilter, size, sort)

Get all MissedEmails in paginated format

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox ID filter | [optional] [default to null]
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageMissedEmailProjection**](../Models/PageMissedEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getMissedEmail"></a>
# **getMissedEmail**
> MissedEmail getMissedEmail(missedEmailId)

Get MissedEmail

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **missedEmailId** | [**UUID**](../Models/)| missedEmailId | [default to null]

### Return type

[**MissedEmail**](../Models/MissedEmail)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="waitForNthMissedEmail"></a>
# **waitForNthMissedEmail**
> MissedEmail waitForNthMissedEmail(inboxId, timeout, index)

Wait for Nth missed email

    Wait for 0 based index missed email

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox ID filter | [default to null]
 **timeout** | **Long**| Optional timeout milliseconds | [default to null]
 **index** | **Integer**| Zero based index of the email to wait for. If 1 missed email already and you want to wait for the 2nd email pass index&#x3D;1 | [optional] [default to null]

### Return type

[**MissedEmail**](../Models/MissedEmail)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

