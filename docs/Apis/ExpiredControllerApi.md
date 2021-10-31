# ExpiredControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getExpirationDefaults**](ExpiredControllerApi#getExpirationDefaults) | **GET** /expired/defaults | Get default expiration settings
[**getExpiredInboxByInboxId**](ExpiredControllerApi#getExpiredInboxByInboxId) | **GET** /expired/inbox/{inboxId} | Get expired inbox record for a previously existing inbox
[**getExpiredInboxRecord**](ExpiredControllerApi#getExpiredInboxRecord) | **GET** /expired/{expiredId} | Get an expired inbox record
[**getExpiredInboxes**](ExpiredControllerApi#getExpiredInboxes) | **GET** /expired | List records of expired inboxes


<a name="getExpirationDefaults"></a>
# **getExpirationDefaults**
> ExpirationDefaults getExpirationDefaults()

Get default expiration settings

    Return default times used for inbox expiration

### Parameters
This endpoint does not need any parameter.

### Return type

[**ExpirationDefaults**](../Models/ExpirationDefaults)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getExpiredInboxByInboxId"></a>
# **getExpiredInboxByInboxId**
> ExpiredInboxDto getExpiredInboxByInboxId(inboxId)

Get expired inbox record for a previously existing inbox

    Use the inboxId to return an ExpiredInboxRecord if an inbox has expired. Inboxes expire and are disabled if an expiration date is set or plan requires. Returns 404 if no expired inbox is found for the inboxId

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| ID of inbox you want to retrieve (not the inbox ID) | [default to null]

### Return type

[**ExpiredInboxDto**](../Models/ExpiredInboxDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getExpiredInboxRecord"></a>
# **getExpiredInboxRecord**
> ExpiredInboxDto getExpiredInboxRecord(expiredId)

Get an expired inbox record

    Inboxes created with an expiration date will expire after the given date and be moved to an ExpiredInbox entity. You can still read emails in the inbox but it can no longer send or receive emails. Fetch the expired inboxes to view the old inboxes properties

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **expiredId** | [**UUID**](../Models/)| ID of the ExpiredInboxRecord you want to retrieve. This is different from the ID of the inbox you are interested in. See other methods for getting ExpiredInboxRecord for an inbox inboxId) | [default to null]

### Return type

[**ExpiredInboxDto**](../Models/ExpiredInboxDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getExpiredInboxes"></a>
# **getExpiredInboxes**
> PageExpiredInboxRecordProjection getExpiredInboxes(before, page, since, size, sort)

List records of expired inboxes

    Inboxes created with an expiration date will expire after the given date. An ExpiredInboxRecord is created that records the inboxes old ID and email address. You can still read emails in the inbox (using the inboxes old ID) but the email address associated with the inbox can no longer send or receive emails. Fetch expired inbox records to view the old inboxes properties

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox sent email list pagination | [optional] [default to 0]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **size** | **Integer**| Optional page size in inbox sent email list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageExpiredInboxRecordProjection**](../Models/PageExpiredInboxRecordProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

