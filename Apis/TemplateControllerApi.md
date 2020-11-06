# TemplateControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTemplate**](TemplateControllerApi.md#createTemplate) | **POST** /templates | Create a Template
[**deleteTemplate**](TemplateControllerApi.md#deleteTemplate) | **DELETE** /templates/{TemplateId} | Delete Template
[**getAllTemplates**](TemplateControllerApi.md#getAllTemplates) | **GET** /templates/paginated | Get all Templates in paginated format
[**getTemplate**](TemplateControllerApi.md#getTemplate) | **GET** /templates/{TemplateId} | Get Template
[**getTemplates**](TemplateControllerApi.md#getTemplates) | **GET** /templates | Get all Templates


<a name="createTemplate"></a>
# **createTemplate**
> TemplateDto createTemplate(createTemplateOptions)

Create a Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createTemplateOptions** | [**CreateTemplateOptions**](..//Models/CreateTemplateOptions.md)| createTemplateOptions |

### Return type

[**TemplateDto**](..//Models/TemplateDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteTemplate"></a>
# **deleteTemplate**
> deleteTemplate(templateId)

Delete Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | [**UUID**](..//Models/.md)| TemplateId | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getAllTemplates"></a>
# **getAllTemplates**
> Page«TemplateProjection» getAllTemplates(page, size, sort)

Get all Templates in paginated format

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in inbox list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**Page«TemplateProjection»**](..//Models/Page«TemplateProjection».md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTemplate"></a>
# **getTemplate**
> TemplateDto getTemplate(templateId)

Get Template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | [**UUID**](..//Models/.md)| TemplateId | [default to null]

### Return type

[**TemplateDto**](..//Models/TemplateDto.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTemplates"></a>
# **getTemplates**
> List getTemplates()

Get all Templates

### Parameters
This endpoint does not need any parameter.

### Return type

[**List**](..//Models/TemplateProjection.md)

### Authorization

[API_KEY](../README.md#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

