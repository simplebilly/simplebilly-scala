

# StockTransfer


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**lineItems** | **AnyType** | JSON array of &#x60;{product_id, name, quantity, batch_number?}&#x60;. | 
**notes** | **String** |  |  [optional]
**sourceWarehouseId** | **String** | References the warehouse entity. | 
**status** | **StockTransferStatus** | One of: draft | completed | cancelled | 
**targetWarehouseId** | **String** | References the warehouse entity. | 
**transferDate** | **LocalDate** |  | 
**transferNumber** | **String** |  | 



