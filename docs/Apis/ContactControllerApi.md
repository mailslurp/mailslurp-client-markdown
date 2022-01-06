# ContactControllerApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createContact**](ContactControllerApi#createContact) | **POST** /contacts | Create a contact
[**deleteContact**](ContactControllerApi#deleteContact) | **DELETE** /contacts/{contactId} | Delete contact
[**getAllContacts**](ContactControllerApi#getAllContacts) | **GET** /contacts/paginated | Get all contacts
[**getContact**](ContactControllerApi#getContact) | **GET** /contacts/{contactId} | Get contact
[**getContactVCard**](ContactControllerApi#getContactVCard) | **GET** /contacts/{contactId}/download | Get contact vCard vcf file
[**getContacts**](ContactControllerApi#getContacts) | **GET** /contacts | Get all contacts


<a name="createContact"></a>
# **createContact**
> ContactDto createContact(CreateContactOptions)

Create a contact

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateContactOptions** | [**CreateContactOptions**](../Models/CreateContactOptions)|  |

### Return type

[**ContactDto**](../Models/ContactDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="deleteContact"></a>
# **deleteContact**
> deleteContact(contactId)

Delete contact

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contactId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllContacts"></a>
# **getAllContacts**
> PageContactProjection getAllContacts(page, size, sort, since, before)

Get all contacts

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageContactProjection**](../Models/PageContactProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getContact"></a>
# **getContact**
> ContactDto getContact(contactId)

Get contact

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contactId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**ContactDto**](../Models/ContactDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getContactVCard"></a>
# **getContactVCard**
> List getContactVCard(contactId)

Get contact vCard vcf file

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contactId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**List**](../Models/ByteArray)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getContacts"></a>
# **getContacts**
> List getContacts()

Get all contacts

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](../Models/ContactProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

