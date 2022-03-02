# BounceControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**filterBouncedRecipient**](BounceControllerApi#filterBouncedRecipient) | **POST** /bounce/filter-recipients | Filter a list of email recipients and remove those who have bounced
[**getBouncedEmail**](BounceControllerApi#getBouncedEmail) | **GET** /bounce/emails/{id} | Get a bounced email.
[**getBouncedEmails**](BounceControllerApi#getBouncedEmails) | **GET** /bounce/emails | Get paginated list of bounced emails.
[**getBouncedRecipient**](BounceControllerApi#getBouncedRecipient) | **GET** /bounce/recipients/{id} | Get a bounced email.
[**getBouncedRecipients**](BounceControllerApi#getBouncedRecipients) | **GET** /bounce/recipients | Get paginated list of bounced recipients.


<a name="filterBouncedRecipient"></a>
# **filterBouncedRecipient**
> FilterBouncedRecipientsResult filterBouncedRecipient(FilterBouncedRecipientsOptions)

Filter a list of email recipients and remove those who have bounced

    Prevent email sending errors by remove recipients who have resulted in past email bounces or complaints

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **FilterBouncedRecipientsOptions** | [**FilterBouncedRecipientsOptions**](../Models/FilterBouncedRecipientsOptions)|  |

### Return type

[**FilterBouncedRecipientsResult**](../Models/FilterBouncedRecipientsResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="getBouncedEmail"></a>
# **getBouncedEmail**
> BouncedEmailDto getBouncedEmail(id)

Get a bounced email.

    Bounced emails are email you have sent that were rejected by a recipient

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of the bounced email to fetch | [default to null]

### Return type

[**BouncedEmailDto**](../Models/BouncedEmailDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getBouncedEmails"></a>
# **getBouncedEmails**
> PageBouncedEmail getBouncedEmails(page, size, sort, since, before)

Get paginated list of bounced emails.

    Bounced emails are email you have sent that were rejected by a recipient

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index | [optional] [default to 0]
 **size** | **Integer**| Optional page size  | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageBouncedEmail**](../Models/PageBouncedEmail)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getBouncedRecipient"></a>
# **getBouncedRecipient**
> BouncedRecipientDto getBouncedRecipient(id)

Get a bounced email.

    Bounced emails are email you have sent that were rejected by a recipient

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of the bounced recipient | [default to null]

### Return type

[**BouncedRecipientDto**](../Models/BouncedRecipientDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getBouncedRecipients"></a>
# **getBouncedRecipients**
> PageBouncedRecipients getBouncedRecipients(page, size, sort, since, before)

Get paginated list of bounced recipients.

    Bounced recipients are email addresses that you have sent emails to that did not accept the sent email. Once a recipient is bounced you cannot send emails to that address.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index  | [optional] [default to 0]
 **size** | **Integer**| Optional page size  | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageBouncedRecipients**](../Models/PageBouncedRecipients)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

