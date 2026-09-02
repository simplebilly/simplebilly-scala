

# ProformaInvoiceUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**convertedAt** | **OffsetDateTime** |  |  [optional]
**convertedToInvoiceId** | **String** | Set when the proforma was converted into a real invoice. References the invoice entity. |  [optional]
**currency** | **CurrencyCode** |  |  [optional]
**customerId** | **String** | References the customer entity. |  [optional]
**customerSnapshot** | **AnyType** | Snapshot of the recipient at issue time (address, VAT id, …). |  [optional]
**issueDate** | **LocalDate** |  |  [optional]
**lineItems** | **AnyType** |  |  [optional]
**notes** | **String** |  |  [optional]
**orderNumber** | **String** | Reference to the order/quote this proforma belongs to. |  [optional]
**paymentDueDate** | **LocalDate** | Optional deadline the real invoice should carry after conversion. |  [optional]
**quotationId** | **String** | References the quotation entity. |  [optional]
**status** | **ProformaInvoiceStatus** | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. |  [optional]
**subtotal** | **String** |  |  [optional]
**totalAmount** | **String** |  |  [optional]
**totalTax** | **String** |  |  [optional]



