# Inbox
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createdAt** | [**Date**](DateTime.md) | When was the inbox created | [optional] [default to null]
**description** | [**String**](string.md) | Optional description of an inbox for labelling purposes | [optional] [default to null]
**emailAddress** | [**String**](string.md) | The inbox&#39;s email address. Send an email to this address and the inbox will receive and store it for you. To retrieve the email use the Inbox and Email Controller endpoints. | [optional] [default to null]
**expiresAt** | [**String**](string.md) | When, if ever, will the inbox expire and be deleted. If null then this inbox is permanent and the emails in it won&#39;t be deleted. Timestamp passed as string. | [optional] [default to null]
**favourite** | [**Boolean**](boolean.md) | Is the inbox favourited | [optional] [default to null]
**id** | [**UUID**](UUID.md) | ID of the inbox | [optional] [default to null]
**name** | [**String**](string.md) | Optional name of the inbox. Displayed in the dashboard for easier search | [optional] [default to null]
**tags** | [**List**](string.md) | Tags that inbox has been tagged with | [optional] [default to null]
**userId** | [**UUID**](UUID.md) | ID of user that inbox belongs to | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

