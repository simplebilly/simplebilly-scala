

# Rfq


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** |  |  [optional]
**lineItems** | **AnyType** | JSON array of &#x60;{product_id, name, sku, quantity, requested_unit_price?, quoted_unit_price?}&#x60;. | 
**notes** | **String** |  |  [optional]
**requestedDate** | **LocalDate** |  | 
**responseDate** | **LocalDate** |  |  [optional]
**rfqNumber** | **String** |  | 
**status** | **RfqStatus** | One of: draft | sent | offer_received | rejected | converted | 
**supplierContactId** | **String** | References the supplier entity. |  [optional]
**supplierName** | **String** |  |  [optional]



