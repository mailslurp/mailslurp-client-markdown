# UpdateInboxOptions
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | [**String**](string) | Name of the inbox and used as the sender name when sending emails .Displayed in the dashboard for easier search | [optional] [default to null]
**description** | [**String**](string) | Description of an inbox for labelling and searching purposes | [optional] [default to null]
**tags** | [**Set**](string) | Tags that inbox has been tagged with. Tags can be added to inboxes to group different inboxes within an account. You can also search for inboxes by tag in the dashboard UI. | [optional] [default to null]
**expiresAt** | [**Date**](DateTime) | Inbox expiration time. When, if ever, the inbox should expire and be deleted. If null then this inbox is permanent and the emails in it won&#39;t be deleted. This is the default behavior unless expiration date is set. If an expiration date is set and the time is reached MailSlurp will expire the inbox and move it to an expired inbox entity. You can still access the emails belonging to it but it can no longer send or receive email. | [optional] [default to null]
**favourite** | [**Boolean**](boolean) | Is the inbox a favorite inbox. Make an inbox a favorite is typically done in the dashboard for quick access or filtering | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

