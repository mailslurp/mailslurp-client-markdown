# TemplateControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTemplate**](TemplateControllerApi#createTemplate) | **POST** /templates | Create a Template
[**deleteTemplate**](TemplateControllerApi#deleteTemplate) | **DELETE** /templates/{templateId} | Delete Template
[**getAllTemplates**](TemplateControllerApi#getAllTemplates) | **GET** /templates/paginated | Get all Templates in paginated format
[**getTemplate**](TemplateControllerApi#getTemplate) | **GET** /templates/{templateId} | Get Template
[**getTemplates**](TemplateControllerApi#getTemplates) | **GET** /templates | Get all Templates
[**updateTemplate**](TemplateControllerApi#updateTemplate) | **PUT** /templates/{templateId} | Update a Template


<a name="createTemplate"></a>
# **createTemplate**
> TemplateDto createTemplate(CreateTemplateOptions)

Create a Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateTemplateOptions** | [**CreateTemplateOptions**](../Models/CreateTemplateOptions)|  |

### Return type

[**TemplateDto**](../Models/TemplateDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="deleteTemplate"></a>
# **deleteTemplate**
> deleteTemplate(templateId)

Delete Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | [**UUID**](../Models/)|  | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllTemplates"></a>
# **getAllTemplates**
> PageTemplateProjection getAllTemplates(page, size, sort, since, before)

Get all Templates in paginated format

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageTemplateProjection**](../Models/PageTemplateProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTemplate"></a>
# **getTemplate**
> TemplateDto getTemplate(templateId)

Get Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**TemplateDto**](../Models/TemplateDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTemplates"></a>
# **getTemplates**
> List getTemplates()

Get all Templates

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](../Models/TemplateProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="updateTemplate"></a>
# **updateTemplate**
> TemplateDto updateTemplate(templateId, CreateTemplateOptions)

Update a Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | [**UUID**](../Models/)|  | [default to null]
 **CreateTemplateOptions** | [**CreateTemplateOptions**](../Models/CreateTemplateOptions)|  |

### Return type

[**TemplateDto**](../Models/TemplateDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

