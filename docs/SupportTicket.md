

# SupportTicket


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assignedTo** | **UUID** |  |  [optional]
**channelId** | **UUID** |  |  [optional]
**channelType** | **SupportChannelType** |  |  [optional]
**closedAt** | **OffsetDateTime** |  |  [optional]
**createdAt** | **OffsetDateTime** |  | 
**customerEmail** | **String** |  |  [optional]
**customerId** | **String** | References the customer entity. |  [optional]
**customerName** | **String** |  |  [optional]
**externalId** | **String** |  |  [optional]
**firstMessageAt** | **OffsetDateTime** |  | 
**lastMessageAt** | **OffsetDateTime** |  | 
**leadId** | **UUID** | References the lead entity. |  [optional]
**messageCount** | **Int** |  | 
**orderRef** | **String** |  |  [optional]
**priority** | **TicketPriority** |  | 
**resolution** | **String** |  |  [optional]
**status** | **SupportTicketStatus** |  | 
**subject** | **String** |  | 
**tags** | **AnyType** |  | 
**tenantId** | **UUID** |  | 
**updatedAt** | **OffsetDateTime** |  |  [optional]



