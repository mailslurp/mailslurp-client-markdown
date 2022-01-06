# MissedEmailControllerApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllMissedEmails**](MissedEmailControllerApi#getAllMissedEmails) | **GET** /missed-emails | Get all MissedEmails in paginated format
[**getAllUnknownMissedEmails**](MissedEmailControllerApi#getAllUnknownMissedEmails) | **GET** /missed-emails/unknown | Get all unknown missed emails in paginated format
[**getMissedEmail**](MissedEmailControllerApi#getMissedEmail) | **GET** /missed-emails/{missedEmailId} | Get MissedEmail
[**waitForNthMissedEmail**](MissedEmailControllerApi#waitForNthMissedEmail) | **GET** /missed-emails/waitForNthMissedEmail | Wait for Nth missed email


<a name="getAllMissedEmails"></a>
# **getAllMissedEmails**
> PageMissedEmailProjection getAllMissedEmails(page, size, sort, searchFilter, since, before, inboxId)

Get all MissedEmails in paginated format

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **inboxId** | [**UUID**](../Models/)| Optional inbox ID filter | [optional] [default to null]

### Return type

[**PageMissedEmailProjection**](../Models/PageMissedEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getAllUnknownMissedEmails"></a>
# **getAllUnknownMissedEmails**
> PageUnknownMissedEmailProjection getAllUnknownMissedEmails(page, size, sort, searchFilter, since, before, inboxId)

Get all unknown missed emails in paginated format

    Unknown missed emails are emails that were sent to MailSlurp but could not be assigned to an existing inbox.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **inboxId** | [**UUID**](../Models/)| Optional inbox ID filter | [optional] [default to null]

### Return type

[**PageUnknownMissedEmailProjection**](../Models/PageUnknownMissedEmailProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getMissedEmail"></a>
# **getMissedEmail**
> MissedEmail getMissedEmail(missedEmailId)

Get MissedEmail

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **missedEmailId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**MissedEmail**](../Models/MissedEmail)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="waitForNthMissedEmail"></a>
# **waitForNthMissedEmail**
> MissedEmail waitForNthMissedEmail(index, inboxId, timeout, since, before)

Wait for Nth missed email

    Wait for 0 based index missed email

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **index** | **Integer**| Zero based index of the email to wait for. If 1 missed email already and you want to wait for the 2nd email pass index&#x3D;1 | [default to null]
 **inboxId** | [**UUID**](../Models/)| Optional inbox ID filter | [optional] [default to null]
 **timeout** | **Long**| Optional timeout milliseconds | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**MissedEmail**](../Models/MissedEmail)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

