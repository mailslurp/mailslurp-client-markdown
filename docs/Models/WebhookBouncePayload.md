# WebhookBouncePayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**bounceId** | [**UUID**](UUID) | ID of the bounce email record. Use the ID with the bounce controller to view more information | [default to null]
**sentToRecipients** | [**List**](string) |  | [optional] [default to null]
**sender** | [**String**](string) |  | [default to null]
**bounceRecipients** | [**List**](string) | Email addresses that resulted in a bounce or email being rejected. Please save these recipients and avoid emailing them in the future to maintain your reputation. | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

