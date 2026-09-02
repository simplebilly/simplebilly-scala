

# GoodsReceipt


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grNumber** | **String** |  | 
**lineItems** | **AnyType** | JSON array of &#x60;{product_id, name, quantity, batch_number?, expiry_date?, bin_location?}&#x60;. | 
**notes** | **String** |  |  [optional]
**purchaseOrderId** | **String** | References the purchase order entity. |  [optional]
**receiptDate** | **LocalDate** |  | 
**supplierContactId** | **String** | References the supplier entity. |  [optional]
**supplierName** | **String** |  |  [optional]
**warehouseId** | **String** | References the warehouse entity. | 



