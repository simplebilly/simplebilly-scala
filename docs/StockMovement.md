

# StockMovement


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delta** | **Long** | Signed movement: positive &#x3D; into stock, negative &#x3D; out of stock. | 
**movementType** | **MovementType** | One of the &#x60;MOVEMENT_*&#x60; constants. | 
**productId** | **UUID** | References the product entity. | 
**quantity** | **Long** | Absolute quantity moved (always &gt;&#x3D; 0). | 
**reason** | **String** |  |  [optional]
**referenceId** | **String** | Primary-key of the referencing entity. |  [optional]
**referenceType** | **ReferenceType** | Entity that caused the movement, e.g. &#x60;goods_receipt&#x60;, &#x60;stock_transfer&#x60;. |  [optional]
**warehouseId** | **String** | References the warehouse entity. | 



