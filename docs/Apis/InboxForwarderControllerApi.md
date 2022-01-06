# InboxForwarderControllerApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewInboxForwarder**](InboxForwarderControllerApi#createNewInboxForwarder) | **POST** /forwarders | Create an inbox forwarder
[**deleteInboxForwarder**](InboxForwarderControllerApi#deleteInboxForwarder) | **DELETE** /forwarders/{id} | Delete an inbox forwarder
[**deleteInboxForwarders**](InboxForwarderControllerApi#deleteInboxForwarders) | **DELETE** /forwarders | Delete inbox forwarders
[**getInboxForwarder**](InboxForwarderControllerApi#getInboxForwarder) | **GET** /forwarders/{id} | Get an inbox forwarder
[**getInboxForwarders**](InboxForwarderControllerApi#getInboxForwarders) | **GET** /forwarders | List inbox forwarders
[**testInboxForwarder**](InboxForwarderControllerApi#testInboxForwarder) | **POST** /forwarders/{id}/test | Test an inbox forwarder
[**testInboxForwardersForInbox**](InboxForwarderControllerApi#testInboxForwardersForInbox) | **PUT** /forwarders | Test inbox forwarders for inbox
[**testNewInboxForwarder**](InboxForwarderControllerApi#testNewInboxForwarder) | **PATCH** /forwarders | Test new inbox forwarder


<a name="createNewInboxForwarder"></a>
# **createNewInboxForwarder**
> InboxForwarderDto createNewInboxForwarder(inboxId, CreateInboxForwarderOptions)

Create an inbox forwarder

    Create a new inbox rule for forwarding, blocking, and allowing emails when sending and receiving

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Inbox id to attach forwarder to | [default to null]
 **CreateInboxForwarderOptions** | [**CreateInboxForwarderOptions**](../Models/CreateInboxForwarderOptions)|  |

### Return type

[**InboxForwarderDto**](../Models/InboxForwarderDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="deleteInboxForwarder"></a>
# **deleteInboxForwarder**
> deleteInboxForwarder(id)

Delete an inbox forwarder

    Delete inbox forwarder

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of inbox forwarder | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteInboxForwarders"></a>
# **deleteInboxForwarders**
> deleteInboxForwarders(inboxId)

Delete inbox forwarders

    Delete inbox forwarders. Accepts optional inboxId filter.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox id to attach forwarder to | [optional] [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getInboxForwarder"></a>
# **getInboxForwarder**
> InboxForwarderDto getInboxForwarder(id)

Get an inbox forwarder

    Get inbox ruleset

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of inbox forwarder | [default to null]

### Return type

[**InboxForwarderDto**](../Models/InboxForwarderDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getInboxForwarders"></a>
# **getInboxForwarders**
> PageInboxForwarderDto getInboxForwarders(inboxId, page, size, sort, searchFilter, since, before)

List inbox forwarders

    List all forwarders attached to an inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox id to get forwarders from | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox forwarder list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox forwarder list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageInboxForwarderDto**](../Models/PageInboxForwarderDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="testInboxForwarder"></a>
# **testInboxForwarder**
> InboxForwarderTestResult testInboxForwarder(id, InboxForwarderTestOptions)

Test an inbox forwarder

    Test an inbox forwarder

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of inbox forwarder | [default to null]
 **InboxForwarderTestOptions** | [**InboxForwarderTestOptions**](../Models/InboxForwarderTestOptions)|  |

### Return type

[**InboxForwarderTestResult**](../Models/InboxForwarderTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="testInboxForwardersForInbox"></a>
# **testInboxForwardersForInbox**
> InboxForwarderTestResult testInboxForwardersForInbox(inboxId, InboxForwarderTestOptions)

Test inbox forwarders for inbox

    Test inbox forwarders for inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| ID of inbox | [default to null]
 **InboxForwarderTestOptions** | [**InboxForwarderTestOptions**](../Models/InboxForwarderTestOptions)|  |

### Return type

[**InboxForwarderTestResult**](../Models/InboxForwarderTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="testNewInboxForwarder"></a>
# **testNewInboxForwarder**
> InboxForwarderTestResult testNewInboxForwarder(TestNewInboxForwarderOptions)

Test new inbox forwarder

    Test new inbox forwarder

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TestNewInboxForwarderOptions** | [**TestNewInboxForwarderOptions**](../Models/TestNewInboxForwarderOptions)|  |

### Return type

[**InboxForwarderTestResult**](../Models/InboxForwarderTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

