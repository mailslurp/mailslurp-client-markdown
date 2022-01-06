# GroupControllerApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addContactsToGroup**](GroupControllerApi#addContactsToGroup) | **PUT** /groups/{groupId}/contacts | Add contacts to a group
[**createGroup**](GroupControllerApi#createGroup) | **POST** /groups | Create a group
[**deleteGroup**](GroupControllerApi#deleteGroup) | **DELETE** /groups/{groupId} | Delete group
[**getAllGroups**](GroupControllerApi#getAllGroups) | **GET** /groups/paginated | Get all Contact Groups in paginated format
[**getGroup**](GroupControllerApi#getGroup) | **GET** /groups/{groupId} | Get group
[**getGroupWithContacts**](GroupControllerApi#getGroupWithContacts) | **GET** /groups/{groupId}/contacts | Get group and contacts belonging to it
[**getGroupWithContactsPaginated**](GroupControllerApi#getGroupWithContactsPaginated) | **GET** /groups/{groupId}/contacts-paginated | 
[**getGroups**](GroupControllerApi#getGroups) | **GET** /groups | Get all groups
[**removeContactsFromGroup**](GroupControllerApi#removeContactsFromGroup) | **DELETE** /groups/{groupId}/contacts | Remove contacts from a group


<a name="addContactsToGroup"></a>
# **addContactsToGroup**
> GroupContactsDto addContactsToGroup(groupId, UpdateGroupContacts)

Add contacts to a group

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | [**UUID**](../Models/)|  | [default to null]
 **UpdateGroupContacts** | [**UpdateGroupContacts**](../Models/UpdateGroupContacts)|  |

### Return type

[**GroupContactsDto**](../Models/GroupContactsDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="createGroup"></a>
# **createGroup**
> GroupDto createGroup(CreateGroupOptions)

Create a group

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateGroupOptions** | [**CreateGroupOptions**](../Models/CreateGroupOptions)|  |

### Return type

[**GroupDto**](../Models/GroupDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="deleteGroup"></a>
# **deleteGroup**
> deleteGroup(groupId)

Delete group

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllGroups"></a>
# **getAllGroups**
> PageGroupProjection getAllGroups(page, size, sort, since, before)

Get all Contact Groups in paginated format

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageGroupProjection**](../Models/PageGroupProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getGroup"></a>
# **getGroup**
> GroupDto getGroup(groupId)

Get group

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**GroupDto**](../Models/GroupDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getGroupWithContacts"></a>
# **getGroupWithContacts**
> GroupContactsDto getGroupWithContacts(groupId)

Get group and contacts belonging to it

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**GroupContactsDto**](../Models/GroupContactsDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getGroupWithContactsPaginated"></a>
# **getGroupWithContactsPaginated**
> PageContactProjection getGroupWithContactsPaginated(groupId, page, size, sort, since, before)



    Get group and paginated contacts belonging to it

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | [**UUID**](../Models/)|  | [default to null]
 **page** | **Integer**| Optional page index in group contact pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in group contact pagination | [optional] [default to 20]
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

<a name="getGroups"></a>
# **getGroups**
> List getGroups()

Get all groups

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](../Models/GroupProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="removeContactsFromGroup"></a>
# **removeContactsFromGroup**
> GroupContactsDto removeContactsFromGroup(groupId, UpdateGroupContacts)

Remove contacts from a group

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | [**UUID**](../Models/)|  | [default to null]
 **UpdateGroupContacts** | [**UpdateGroupContacts**](../Models/UpdateGroupContacts)|  |

### Return type

[**GroupContactsDto**](../Models/GroupContactsDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

