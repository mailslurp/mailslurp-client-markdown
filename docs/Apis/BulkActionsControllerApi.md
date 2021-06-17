# BulkActionsControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulkCreateInboxes**](BulkActionsControllerApi#bulkCreateInboxes) | **POST** /bulk/inboxes | Bulk create Inboxes (email addresses)
[**bulkDeleteInboxes**](BulkActionsControllerApi#bulkDeleteInboxes) | **DELETE** /bulk/inboxes | Bulk Delete Inboxes
[**bulkSendEmails**](BulkActionsControllerApi#bulkSendEmails) | **POST** /bulk/send | Bulk Send Emails


<a name="bulkCreateInboxes"></a>
# **bulkCreateInboxes**
> List bulkCreateInboxes(count)

Bulk create Inboxes (email addresses)

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **count** | **Integer**| Number of inboxes to be created in bulk | [default to null]

### Return type

[**List**](../Models/Inbox)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="bulkDeleteInboxes"></a>
# **bulkDeleteInboxes**
> bulkDeleteInboxes(ids)

Bulk Delete Inboxes

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | [**List**](../Models/UUID)| ids |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

<a name="bulkSendEmails"></a>
# **bulkSendEmails**
> bulkSendEmails(bulkSendEmailOptions)

Bulk Send Emails

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulkSendEmailOptions** | [**BulkSendEmailOptions**](../Models/BulkSendEmailOptions)| bulkSendEmailOptions |

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

