

# TimelineEvent

Single timeline entry aggregated from the contact's activity across all related modules (communications, quotations, orders, invoices, documents).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | **String** | RFC3339 UTC timestamp for sorting. | 
**detail** | **String** |  |  [optional]
**id** | **String** | Source record id (stringified). | 
**status** | **String** |  |  [optional]
**title** | **String** |  | 
**`type`** | **String** | Source module: communication | quotation | order | invoice | attachment. | 



