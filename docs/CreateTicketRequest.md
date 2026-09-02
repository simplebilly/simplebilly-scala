

# CreateTicketRequest

Request body for creating a support ticket. Wraps the generated `SupportTicketCreateDto` fields plus `message_body` which is not a Model field (used to create the initial `ticket_message`).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **UUID** |  |  [optional]
**channelType** | **String** |  |  [optional]
**customerEmail** | **String** |  |  [optional]
**customerId** | **String** |  |  [optional]
**customerName** | **String** |  |  [optional]
**externalId** | **String** |  |  [optional]
**messageBody** | **String** |  | 
**orderRef** | **String** |  |  [optional]
**subject** | **String** |  | 



