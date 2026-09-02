

# ProductionOrderCosting

Actual-costing (Nachkalkulation) report for a production order.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**costPerUnit** | **String** | material_cost_total ÷ quantity. | 
**costSource** | **String** | \&quot;actual\&quot; when costed from stock-movement consumption, else \&quot;planned\&quot;. | 
**lines** | [**Seq&lt;CostingLine&gt;**](CostingLine.md) |  | 
**marginPerUnit** | **String** | sale_price − cost_per_unit. |  [optional]
**marginPercent** | **String** | margin_per_unit ÷ cost_per_unit as a percentage. |  [optional]
**materialCostTotal** | **String** | Total material cost for the whole order. | 
**orderNumber** | **String** |  | 
**productionOrderId** | **UUID** |  | 
**quantity** | **Long** |  | 
**salePrice** | **String** | Finished product&#39;s sale price per unit (used to compute margin). |  [optional]
**status** | **String** |  | 



