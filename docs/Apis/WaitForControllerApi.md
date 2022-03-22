# WaitForControllerApi

All URIs are relative to *https://api.mailslurp.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**waitFor**](WaitForControllerApi#waitFor) | **POST** /waitFor | Wait for an email to match the provided filter conditions such as subject contains keyword.
[**waitForEmailCount**](WaitForControllerApi#waitForEmailCount) | **GET** /waitForEmailCount | Wait for and return count number of emails. Hold connection until inbox count matches expected or timeout occurs
[**waitForLatestEmail**](WaitForControllerApi#waitForLatestEmail) | **GET** /waitForLatestEmail | Fetch inbox&#39;s latest email or if empty wait for an email to arrive
[**waitForMatchingEmails**](WaitForControllerApi#waitForMatchingEmails) | **POST** /waitForMatchingEmails | Wait or return list of emails that match simple matching patterns
[**waitForMatchingFirstEmail**](WaitForControllerApi#waitForMatchingFirstEmail) | **POST** /waitForMatchingFirstEmail | Wait for or return the first email that matches provided MatchOptions array
[**waitForNthEmail**](WaitForControllerApi#waitForNthEmail) | **GET** /waitForNthEmail | Wait for or fetch the email with a given index in the inbox specified. If index doesn&#39;t exist waits for it to exist or timeout to occur.


<a name="waitFor"></a>
# **waitFor**
> List waitFor(WaitForConditions)

Wait for an email to match the provided filter conditions such as subject contains keyword.

    Generic waitFor method that will wait until an inbox meets given conditions or return immediately if already met

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WaitForConditions** | [**WaitForConditions**](../Models/WaitForConditions)|  |

### Return type

[**List**](../Models/EmailPreview)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="waitForEmailCount"></a>
# **waitForEmailCount**
> List waitForEmailCount(inboxId, count, timeout, unreadOnly, before, since, sort, delay)

Wait for and return count number of emails. Hold connection until inbox count matches expected or timeout occurs

    If inbox contains count or more emails at time of request then return count worth of emails. If not wait until the count is reached and return those or return an error if timeout is exceeded.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Id of the inbox we are fetching emails from | [default to null]
 **count** | **Integer**| Number of emails to wait for. Must be greater that 1 | [default to null]
 **timeout** | **Long**| Max milliseconds to wait | [optional] [default to null]
 **unreadOnly** | **Boolean**| Optional filter for unread only | [optional] [default to false]
 **before** | **Date**| Filter for emails that were received before the given timestamp | [optional] [default to null]
 **since** | **Date**| Filter for emails that were received after the given timestamp | [optional] [default to null]
 **sort** | **String**| Sort direction | [optional] [default to null] [enum: ASC, DESC]
 **delay** | **Long**| Max milliseconds delay between calls | [optional] [default to null]

### Return type

[**List**](../Models/EmailPreview)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="waitForLatestEmail"></a>
# **waitForLatestEmail**
> Email waitForLatestEmail(inboxId, timeout, unreadOnly, before, since, sort, delay)

Fetch inbox&#39;s latest email or if empty wait for an email to arrive

    Will return either the last received email or wait for an email to arrive and return that. If you need to wait for an email for a non-empty inbox set &#x60;unreadOnly&#x3D;true&#x60; or see the other receive methods such as &#x60;waitForNthEmail&#x60; or &#x60;waitForEmailCount&#x60;.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Id of the inbox we are fetching emails from | [optional] [default to null]
 **timeout** | **Long**| Max milliseconds to wait | [optional] [default to null]
 **unreadOnly** | **Boolean**| Optional filter for unread only. | [optional] [default to false]
 **before** | **Date**| Filter for emails that were before after the given timestamp | [optional] [default to null]
 **since** | **Date**| Filter for emails that were received after the given timestamp | [optional] [default to null]
 **sort** | **String**| Sort direction | [optional] [default to null] [enum: ASC, DESC]
 **delay** | **Long**| Max milliseconds delay between calls | [optional] [default to null]

### Return type

[**Email**](../Models/Email)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="waitForMatchingEmails"></a>
# **waitForMatchingEmails**
> List waitForMatchingEmails(inboxId, count, MatchOptions, before, since, sort, delay, timeout, unreadOnly)

Wait or return list of emails that match simple matching patterns

    Perform a search of emails in an inbox with the given patterns. If results match expected count then return or else retry the search until results are found or timeout is reached. Match options allow simple CONTAINS or EQUALS filtering on SUBJECT, TO, BCC, CC, and FROM. See the &#x60;MatchOptions&#x60; object for options. An example payload is &#x60;{ matches: [{field: &#39;SUBJECT&#39;,should:&#39;CONTAIN&#39;,value:&#39;needle&#39;}] }&#x60;. You can use an array of matches and they will be applied sequentially to filter out emails. If you want to perform matches and extractions of content using Regex patterns see the EmailController &#x60;getEmailContentMatch&#x60; method.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Id of the inbox we are fetching emails from | [default to null]
 **count** | **Integer**| Number of emails to wait for. Must be greater or equal to 1 | [default to null]
 **MatchOptions** | [**MatchOptions**](../Models/MatchOptions)|  |
 **before** | **Date**| Filter for emails that were received before the given timestamp | [optional] [default to null]
 **since** | **Date**| Filter for emails that were received after the given timestamp | [optional] [default to null]
 **sort** | **String**| Sort direction | [optional] [default to null] [enum: ASC, DESC]
 **delay** | **Long**| Max milliseconds delay between calls | [optional] [default to null]
 **timeout** | **Long**| Max milliseconds to wait | [optional] [default to null]
 **unreadOnly** | **Boolean**| Optional filter for unread only | [optional] [default to false]

### Return type

[**List**](../Models/EmailPreview)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="waitForMatchingFirstEmail"></a>
# **waitForMatchingFirstEmail**
> Email waitForMatchingFirstEmail(inboxId, MatchOptions, timeout, unreadOnly, since, before, sort, delay)

Wait for or return the first email that matches provided MatchOptions array

    Perform a search of emails in an inbox with the given patterns. If a result if found then return or else retry the search until a result is found or timeout is reached. Match options allow simple CONTAINS or EQUALS filtering on SUBJECT, TO, BCC, CC, and FROM. See the &#x60;MatchOptions&#x60; object for options. An example payload is &#x60;{ matches: [{field: &#39;SUBJECT&#39;,should:&#39;CONTAIN&#39;,value:&#39;needle&#39;}] }&#x60;. You can use an array of matches and they will be applied sequentially to filter out emails. If you want to perform matches and extractions of content using Regex patterns see the EmailController &#x60;getEmailContentMatch&#x60; method.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Id of the inbox we are matching an email for | [default to null]
 **MatchOptions** | [**MatchOptions**](../Models/MatchOptions)|  |
 **timeout** | **Long**| Max milliseconds to wait | [optional] [default to null]
 **unreadOnly** | **Boolean**| Optional filter for unread only | [optional] [default to false]
 **since** | **Date**| Filter for emails that were received after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter for emails that were received before the given timestamp | [optional] [default to null]
 **sort** | **String**| Sort direction | [optional] [default to null] [enum: ASC, DESC]
 **delay** | **Long**| Max milliseconds delay between calls | [optional] [default to null]

### Return type

[**Email**](../Models/Email)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="waitForNthEmail"></a>
# **waitForNthEmail**
> Email waitForNthEmail(inboxId, index, timeout, unreadOnly, since, before, sort, delay)

Wait for or fetch the email with a given index in the inbox specified. If index doesn&#39;t exist waits for it to exist or timeout to occur.

    If nth email is already present in inbox then return it. If not hold the connection open until timeout expires or the nth email is received and returned.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inboxId** | [**UUID**](../Models/)| Id of the inbox you are fetching emails from | [optional] [default to null]
 **index** | **Integer**| Zero based index of the email to wait for. If an inbox has 1 email already and you want to wait for the 2nd email pass index&#x3D;1 | [optional] [default to 0]
 **timeout** | **Long**| Max milliseconds to wait for the nth email if not already present | [optional] [default to null]
 **unreadOnly** | **Boolean**| Optional filter for unread only | [optional] [default to false]
 **since** | **Date**| Filter for emails that were received after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter for emails that were received before the given timestamp | [optional] [default to null]
 **sort** | **String**| Sort direction | [optional] [default to null] [enum: ASC, DESC]
 **delay** | **Long**| Max milliseconds delay between calls | [optional] [default to null]

### Return type

[**Email**](../Models/Email)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

