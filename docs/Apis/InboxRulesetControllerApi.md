# InboxRulesetControllerApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewInboxRuleset**](InboxRulesetControllerApi#createNewInboxRuleset) | **POST** /rulesets | Create an inbox ruleset
[**deleteInboxRuleset**](InboxRulesetControllerApi#deleteInboxRuleset) | **DELETE** /rulesets/{id} | Delete an inbox ruleset
[**deleteInboxRulesets**](InboxRulesetControllerApi#deleteInboxRulesets) | **DELETE** /rulesets | Delete inbox rulesets
[**getInboxRuleset**](InboxRulesetControllerApi#getInboxRuleset) | **GET** /rulesets/{id} | Get an inbox ruleset
[**getInboxRulesets**](InboxRulesetControllerApi#getInboxRulesets) | **GET** /rulesets | List inbox rulesets
[**testInboxRuleset**](InboxRulesetControllerApi#testInboxRuleset) | **POST** /rulesets/{id}/test | Test an inbox ruleset
[**testInboxRulesetsForInbox**](InboxRulesetControllerApi#testInboxRulesetsForInbox) | **PUT** /rulesets | Test inbox rulesets for inbox
[**testNewInboxRuleset**](InboxRulesetControllerApi#testNewInboxRuleset) | **PATCH** /rulesets | Test new inbox ruleset


<a name="createNewInboxRuleset"></a>
# **createNewInboxRuleset**
> InboxRulesetDto createNewInboxRuleset(inboxId, CreateInboxRulesetOptions)

Create an inbox ruleset

    Create a new inbox rule for forwarding, blocking, and allowing emails when sending and receiving

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Inbox id to attach ruleset to | [default to null]
 **CreateInboxRulesetOptions** | [**CreateInboxRulesetOptions**](../Models/CreateInboxRulesetOptions)|  |

### Return type

[**InboxRulesetDto**](../Models/InboxRulesetDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

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
- **Accept**: */*

<a name="getInboxRulesets"></a>
# **getInboxRulesets**
> PageInboxRulesetDto getInboxRulesets(inboxId, page, size, sort, searchFilter, since, before)

List inbox rulesets

    List all rulesets attached to an inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Optional inbox id to get rulesets from | [optional] [default to null]
 **page** | **Integer**| Optional page index in inbox ruleset list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in inbox ruleset list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageInboxRulesetDto**](../Models/PageInboxRulesetDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="testInboxRuleset"></a>
# **testInboxRuleset**
> InboxRulesetTestResult testInboxRuleset(id, InboxRulesetTestOptions)

Test an inbox ruleset

    Test an inbox ruleset

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)| ID of inbox ruleset | [default to null]
 **InboxRulesetTestOptions** | [**InboxRulesetTestOptions**](../Models/InboxRulesetTestOptions)|  |

### Return type

[**InboxRulesetTestResult**](../Models/InboxRulesetTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="testInboxRulesetsForInbox"></a>
# **testInboxRulesetsForInbox**
> InboxRulesetTestResult testInboxRulesetsForInbox(inboxId, InboxRulesetTestOptions)

Test inbox rulesets for inbox

    Test inbox rulesets for inbox

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| ID of inbox | [default to null]
 **InboxRulesetTestOptions** | [**InboxRulesetTestOptions**](../Models/InboxRulesetTestOptions)|  |

### Return type

[**InboxRulesetTestResult**](../Models/InboxRulesetTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="testNewInboxRuleset"></a>
# **testNewInboxRuleset**
> InboxRulesetTestResult testNewInboxRuleset(TestNewInboxRulesetOptions)

Test new inbox ruleset

    Test new inbox ruleset

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TestNewInboxRulesetOptions** | [**TestNewInboxRulesetOptions**](../Models/TestNewInboxRulesetOptions)|  |

### Return type

[**InboxRulesetTestResult**](../Models/InboxRulesetTestResult)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

