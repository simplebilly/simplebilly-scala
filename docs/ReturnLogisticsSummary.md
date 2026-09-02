

# ReturnLogisticsSummary

Warehouse-level aggregation for the returns logistics dashboard.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**byStatus** | **AnyType** | Number of return orders per status. | 
**byWarehouse** | [**Seq&lt;ReturnWarehouseSummary&gt;**](ReturnWarehouseSummary.md) | Per-warehouse aggregation. | 
**itemsRestocked** | **Long** | Sum of &#x60;restock: true&#x60; line-item quantities. | 
**itemsScrapped** | **Long** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). | 
**totalItems** | **Long** | Sum of all line-item quantities across returns. | 
**totalReturns** | **Long** | Total number of return orders (excluding soft-deleted). | 



