

# SupplierInvoice


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **String** |  |  [optional]
**goodsReceiptId** | **String** | References the goods receipt entity. |  [optional]
**invoiceDate** | **LocalDate** |  | 
**invoiceNumber** | **String** |  | 
**lineItems** | **AnyType** | JSON array of &#x60;{product_id, name, quantity, unitPriceNet, taxRate}&#x60;. | 
**notes** | **String** |  |  [optional]
**purchaseOrderId** | **String** | References the purchase order entity. |  [optional]
**status** | **SupplierInvoiceStatus** | One of: draft | matched | has_variances | posted | cancelled | 
**supplierContactId** | **String** | References the supplier entity. |  [optional]
**supplierName** | **String** |  |  [optional]
**totalGrossAmount** | **String** |  |  [optional]
**totalNetAmount** | **String** |  |  [optional]



