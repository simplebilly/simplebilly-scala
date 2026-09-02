

# CustomerCommunicationCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **String** | The message body, call summary or note text. |  [optional]
**channel** | **CommunicationChannel** |  | 
**contactId** | **String** | The contact (customer/supplier) this communication belongs to. References the contact entity. | 
**counterparty** | **String** | Email/phone of the counterparty, if applicable. |  [optional]
**direction** | **CommunicationDirection** |  | 
**occurredAt** | **OffsetDateTime** | When the communication happened (defaults to now on create). |  [optional]
**subject** | **String** |  |  [optional]
**tags** | **AnyType** | Free-form tags, e.g. &#x60;[\&quot;follow-up-required\&quot;]&#x60;. |  [optional]



