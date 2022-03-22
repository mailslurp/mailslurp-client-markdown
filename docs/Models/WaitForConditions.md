# WaitForConditions
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**inboxId** | [**UUID**](UUID) | ID of inbox to search within and apply conditions to. Essentially filtering the emails found to give a count. | [default to null]
**count** | [**Integer**](integer) | Number of results that should match conditions. Either exactly or at least this amount based on the &#x60;countType&#x60;. If count condition is not met and the timeout has not been reached the &#x60;waitFor&#x60; method will retry the operation. | [optional] [default to null]
**delayTimeout** | [**Long**](long) | Max time in milliseconds to wait between retries if a &#x60;timeout&#x60; is specified. | [optional] [default to null]
**timeout** | [**Long**](long) | Max time in milliseconds to retry the &#x60;waitFor&#x60; operation until conditions are met. | [default to null]
**unreadOnly** | [**Boolean**](boolean) | Apply conditions only to **unread** emails. All emails begin with &#x60;read&#x3D;false&#x60;. An email is marked &#x60;read&#x3D;true&#x60; when an &#x60;EmailDto&#x60; representation of it has been returned to the user at least once. For example you have called &#x60;getEmail&#x60; or &#x60;waitForLatestEmail&#x60; etc., or you have viewed the email in the dashboard. | [optional] [default to null]
**countType** | [**String**](string) | How result size should be compared with the expected size. Exactly or at-least matching result? | [optional] [default to null]
**matches** | [**List**](MatchOption) | Conditions that should be matched for an email to qualify for results. Each condition will be applied in order to each email within an inbox to filter a result list of matching emails you are waiting for. | [optional] [default to null]
**sortDirection** | [**String**](string) | Direction to sort matching emails by created time | [optional] [default to null]
**since** | [**Date**](DateTime) | ISO Date Time earliest time of email to consider. Filter for matching emails that were received after this date | [optional] [default to null]
**before** | [**Date**](DateTime) | ISO Date Time latest time of email to consider. Filter for matching emails that were received before this date | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

