# InboxRulesetControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewInboxRuleset**](InboxRulesetControllerApi#createNewInboxRuleset) | **POST** /rulesets | Create an inbox ruleset
[**deleteInboxRuleset**](InboxRulesetControllerApi#deleteInboxRuleset) | **DELETE** /rulesets/{id} | Delete an inbox ruleset
[**deleteInboxRulesets**](InboxRulesetControllerApi#deleteInboxRulesets) | **DELETE** /rulesets | Delete inbox rulesets
[**getInboxRuleset**](InboxRulesetControllerApi#getInboxRuleset) | **GET** /rulesets/{id} | Get an inbox ruleset
[**getInboxRulesets**](InboxRulesetControllerApi#getInboxRulesets) | **GET** /rulesets | List inbox rulesets


<a name="createNewInboxRuleset"></a>
# **createNewInboxRuleset**
> InboxRulesetDto createNewInboxRuleset(createInboxRulesetOptions, inboxId)

Create an inbox ruleset

    Create a new inbox rule for forwarding, blocking, and allowing emails when sending and receiving

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createInboxRulesetOptions** | [**CreateInboxRulesetOptions**](../Models/CreateInboxRulesetOptions)| createInboxRulesetOptions |
 **inboxId** | [**UUID**](../Models/)| Inbox id to attach ruleset to | [optional] [default to null]

### Return type

[**InboxRulesetDto**](../Models/InboxRulesetDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteInboxRuleset"></a>
# **deleteInboxRuleset**
> deleteInboxRuleset(id)

Delete an inbox ruleset

    Delete inbox ruleset

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of inbox ruleset | [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="deleteInboxRulesets"></a>
# **deleteInboxRulesets**
> deleteInboxRulesets(inboxId)

Delete inbox rulesets

    Delete inbox rulesets. Accepts optional inboxId filter.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox id to attach ruleset to | [optional] [default to null]

### Return type

null (empty response body)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

<a name="getInboxRuleset"></a>
# **getInboxRuleset**
> InboxRulesetDto getInboxRuleset(id)

Get an inbox ruleset

    Get inbox ruleset

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of inbox ruleset | [default to null]

### Return type

[**InboxRulesetDto**](../Models/InboxRulesetDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getInboxRulesets"></a>
# **getInboxRulesets**
> PageInboxRulesetProjection getInboxRulesets(inboxId, page, size, sort)

List inbox rulesets

    List all rulesets attached to an inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox id to get rulesets from | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox ruleset list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox ruleset list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]

### Return type

[**PageInboxRulesetProjection**](../Models/PageInboxRulesetProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

