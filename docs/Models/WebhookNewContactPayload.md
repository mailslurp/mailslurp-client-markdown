# WebhookNewContactPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | [**String**](string) | Idempotent message ID. Store this ID locally or in a database to prevent message duplication. | [default to null]
**webhookId** | [**UUID**](UUID) | ID of webhook entity being triggered | [default to null]
**webhookName** | [**String**](string) | Name of the webhook being triggered | [optional] [default to null]
**eventName** | [**String**](string) | Name of the event type webhook is being triggered for. | [default to null]
**contactId** | [**UUID**](UUID) |  | [default to null]
**groupId** | [**UUID**](UUID) |  | [optional] [default to null]
**firstName** | [**String**](string) |  | [optional] [default to null]
**lastName** | [**String**](string) |  | [optional] [default to null]
**company** | [**String**](string) |  | [optional] [default to null]
**primaryEmailAddress** | [**String**](string) |  | [optional] [default to null]
**emailAddresses** | [**List**](string) |  | [default to null]
**tags** | [**List**](string) |  | [default to null]
**metaData** | [**Object**]() |  | [optional] [default to null]
**optOut** | [**Boolean**](boolean) |  | [optional] [default to null]
**createdAt** | [**Date**](DateTime) |  | [default to null]

[[Back to Model list]](../README#documentation-for-models) [[Back to API list]](../README#documentation-for-api-endpoints) [[Back to README]](../README)

