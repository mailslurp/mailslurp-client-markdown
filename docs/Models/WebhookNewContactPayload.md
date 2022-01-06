# WebhookNewContactPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [optional] [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [optional] [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [optional] [default to null]
**contactId** | [**UUID**](UUID) |  | [optional] [default to null]
**groupId** | [**UUID**](UUID) |  | [optional] [default to null]
**firstName** | [**String**](string) |  | [optional] [default to null]
**lastName** | [**String**](string) |  | [optional] [default to null]
**company** | [**String**](string) |  | [optional] [default to null]
**primaryEmailAddress** | [**String**](string) |  | [optional] [default to null]
**emailAddresses** | [**Set**](string) |  | [optional] [default to null]
**tags** | [**Set**](string) |  | [optional] [default to null]
**metaData** | [**Object**]() |  | [optional] [default to null]
**optOut** | [**Boolean**](boolean) |  | [optional] [default to null]
**createdAt** | [**Date**](DateTime) |  | [optional] [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

