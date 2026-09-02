

# PurchaseOrderUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** |  |  [optional]
**deliveryAddress** | **AnyType** |  |  [optional]
**expectedDeliveryDate** | **LocalDate** |  |  [optional]
**lineItems** | **AnyType** | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. |  [optional]
**notes** | **String** |  |  [optional]
**orderDate** | **LocalDate** |  |  [optional]
**poNumber** | **String** |  |  [optional]
**status** | **PurchaseOrderStatus** | One of: draft | ordered | partially_received | received | cancelled |  [optional]
**supplierContactId** | **String** | References the supplier entity. |  [optional]
**supplierName** | **String** |  |  [optional]
**totalGrossAmount** | **String** |  |  [optional]
**totalNetAmount** | **String** |  |  [optional]



